# Basic API

---

#### To get started we will have to create a very simple server which can handle HTTP requests. To do this we’ll create a new file called main.go. Within this main.go file we’ll want to define 3 distinct functions. A homePage function that will handle all requests to our root URL, a handleRequests function that will match the URL path hit with a defined function and a main function which will kick off our API.

    main.go

    package main

    import (
        "fmt"
        "log"
        "net/http"
    )

    func homePage(w http.ResponseWriter, r *http.Request){
        fmt.Fprintf(w, "Welcome to the HomePage!")
        fmt.Println("Endpoint Hit: homePage")
    }

    func handleRequests() {
        http.HandleFunc("/", homePage)
        log.Fatal(http.ListenAndServe(":10000", nil))
    }

    func main() {
        handleRequests()
    }

#### If we run this on our machine now, we should see our very simple API start up on port 10000 if it’s not already been taken by another process. If we now navigate to http://localhost:10000/ in our local browser we should see Welcome to the HomePage! print out on our screen. This means we have successfully created the base from which we’ll build our REST API.

### Our Articles Structure

#### We’ll be creating a REST API that allows us to CREATE, READ, UPDATE and DELETE the articles on our website. When we talk about CRUD APIs we are referring to an API that can handle all of these tasks: Creating, Reading, Updating and Deleting.

#### Before we can get started, we’ll have to define our Article structure. Go has this concept of structs that are perfect for just this scenario. Let’s create an Article struct that features a Title, a Description (desc) and Content like so:

    type Article struct {
        Title string `json:"Title"`
        Desc string `json:"desc"`
        Content string `json:"content"`
    }

    // let's declare a global Articles array
    // that we can then populate in our main function
    // to simulate a database
    var Articles []Article

#### Our Struct contains the 3 properties we need to represent all of the articles on our site. In order for this to work, we’ll also have to import the "encoding/json" package into our list of imports.

#### Let’s now update our main function so that our Articles variable is populated with some dummy data that we can retrieve and modify later on.

    func main() {
        Articles = []Article{
            Article{Title: "Hello", Desc: "Article Description", Content: "Article Content"},
            Article{Title: "Hello 2", Desc: "Article Description", Content: "Article Content"},
        }
        handleRequests()
    }

#### Perfect, let’s now move on to creating our /articles endpoint which will return all of the articles that we’ve just defined here.

---

## Getting Started with Routers

Now the standard library is adequate at providing everything you need to get your own simple REST API up and running but now that we’ve got the basic concepts down I feel it’s time to introduce third-party router packages. The most notable and highly used is the gorilla/mux router which, as it stands currently has 2,281 stars on Github.

### Building our Router

We can update our existing main.go file and swap in a gorilla/mux based HTTP router in place of the standard library one which was present before.

#### Modify your handleRequests function so that it creates a new router.

    main.go

    package main

    import (
        "fmt"
        "log"
        "net/http"
        "encoding/json"
        "github.com/gorilla/mux"
    )

    … // Existing code from above
    func handleRequests() {
        // creates a new instance of a mux router
        myRouter := mux.NewRouter().StrictSlash(true)
        // replace http.HandleFunc with myRouter.HandleFunc
        myRouter.HandleFunc("/", homePage)
        myRouter.HandleFunc("/all", returnAllArticles)
        // finally, instead of passing in nil, we want
        // to pass in our newly created router as the second
        // argument
        log.Fatal(http.ListenAndServe(":10000", myRouter))
    }

    func main() {
        fmt.Println("Rest API v2.0 - Mux Routers")
        Articles = []Article{
            Article{Title: "Hello", Desc: "Article Description", Content: "Article Content"},
            Article{Title: "Hello 2", Desc: "Article Description", Content: "Article Content"},
        }
        handleRequests()
    }

#### When you now run this, you will see no real change to the way our system works. It will still start up on the same port and return the same results depending on what endpoints you hit.

#### The only real difference is that we now have a gorilla/mux router which will allow us to easily do things such as retrieve path and query parameters later on in this tutorial.

    $ go run main.go

    Rest API v2.0 - Mux Routers

### Path Variables

#### So far so good, we’ve created a very simple REST API that returns a homepage and all our Articles. But what happens if we want to just view one article?

#### Well, thanks to the gorilla mux router we can add variables to our paths and then pick and choose what articles we want to return based on these variables. Create a new route within your handleRequests() function just below our /articles route:

    myRouter.HandleFunc("/article/{id}", returnSingleArticle)

#### Notice that we’ve added {id} to our path. This will represent our id variable that we’ll be able to use when we wish to return only the article that features that exact key. For now, our Article struct doesn’t feature an Id property. Let’s add that now:

    type Article struct {
        Id      string `json:"Id"`
        Title   string `json:"Title"`
        Desc    string `json:"desc"`
        Content string `json:"content"`
    }

#### We can then update our main function to populate our Id values in our Articles array:

    func main() {
        Articles = []Article{
            Article{Id: "1", Title: "Hello", Desc: "Article Description", Content: "Article Content"},
            Article{Id: "2", Title: "Hello 2", Desc: "Article Description", Content: "Article Content"},
        }
        handleRequests()
    }

#### Now that we’ve done that, in our returnSingleArticle function we can obtain this {id} value from our URL and we can return the article that matches this criteria. As we haven’t stored our data anywhere we’ll just be returning the Id that was passed to the browser.

    func returnSingleArticle(w http.ResponseWriter, r *http.Request){
        vars := mux.Vars(r)
        key := vars["id"]

        fmt.Fprintf(w, "Key: " + key)
    }

#### If we navigate to http://localhost:1000/article/1after we’ve now run this, you should see Key: 1 being printed out within the browser.

#### Let’s use this key value to return the specific article that matches that key.

    func returnSingleArticle(w http.ResponseWriter, r *http.Request) {
        vars := mux.Vars(r)
        key := vars["id"]

        // Loop over all of our Articles
        // if the article.Id equals the key we pass in
        // return the article encoded as JSON
        for _, article := range Articles {
            if article.Id == key {
                json.NewEncoder(w).Encode(article)
            }
        }
    }
