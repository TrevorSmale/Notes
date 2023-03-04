# Basic server

---

Use Go version 1.11 or higher.

#### Create the following files and folders according to the structure below. The file server.go sits at the root of your project, as does the static folder, which contains two HTML files: index.html and form.html.

    - server.go
    - static/
    - - index.html
    - - form.html

#### Open the server.go file and import the required packages. Use fmt to print useful data to the terminal and log to print fatal errors in case the web server crashes.

#### The net/http is the most important package. It provides all the functionality for creating an HTTP client or server implementation such as a Golang web server.

    package main

    import (
        "fmt"
        "log"
        "net/http"
    )

#### Lastly, let’s add a simple main() function in the server.go file that prints a message to the terminal.

    func main() {
        fmt.Printf("Starting server at port 8080\n")
    }

#### To test the setup, start the fictive server with the following command.

    go run server.go

---