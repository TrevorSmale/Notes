# Retrieving All Articles

---

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