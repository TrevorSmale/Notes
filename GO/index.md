# Go
## Golang notes

### [Packaging Modules](Gopackage.md)
### [Go Server](Goserv.md)
### [Go API](GoAPI.md)



## Retrieving All Articles

#### In this part of the tutorial we are going to create a new REST endpoint which, when hit with a HTTP GET request, will return all of the articles for our site.

#### We’ll first start off by creating a new function called returnAllArticles, which will do the simple task of returning our newly populated Articles variable, encoded in JSON format:

    main.go

    func returnAllArticles(w http.ResponseWriter, r *http.Request){
        fmt.Println("Endpoint Hit: returnAllArticles")
        json.NewEncoder(w).Encode(Articles)
    }

#### The call to json.NewEncoder(w).Encode(article) does the job of encoding our articles array into a JSON string and then writing as part of our response.

#### Before this will work, we’ll also need to add a new route to our handleRequests function that will map any calls to http://localhost:10000/articles to our newly defined function.

    func handleRequests() {
        http.HandleFunc("/", homePage)
        // add our articles route and map it to our 
        // returnAllArticles function like so
        http.HandleFunc("/articles", returnAllArticles)
        log.Fatal(http.ListenAndServe(":10000", nil))
    }

#### Now that we’ve done this, run the code by typing go run main.go and then open up http://localhost:10000/articles in your browser and you should see a JSON representation of your list of articles like so:

    http://localhost:10000/articles response

    [
    {
        Title: "Hello",
        desc: "Article Description",
        content: "Article Content"
    },
    {
        Title: "Hello 2",
        desc: "Article Description",
        content: "Article Content"
    }
    ];

#### We’ve successfully defined our first API endpoint.

#### In the next part of this series, you are going to update your REST API to use a gorilla/mux router instead of the traditional net/http router.

#### Swapping the routers will enable you to more easily perform tasks such as parsing any path or query parameters that may reside within an incoming HTTP request which we will need later on.

---

## Getting Started with Routers

#### Now the standard library is adequate at providing everything you need to get your own simple REST API up and running but now that we’ve got the basic concepts down I feel it’s time to introduce third-party router packages. The most notable and highly used is the gorilla/mux router which, as it stands currently has 2,281 stars on Github.

### Building our Router

#### We can update our existing main.go file and swap in a gorilla/mux based HTTP router in place of the standard library one which was present before.

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
