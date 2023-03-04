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