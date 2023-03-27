# JSON READ
## Importing, Unmarshalling and Interpreting JSON string data

Let’s assume a simple file config.json, having the following content:

    {
        "origin": "golangdocs.com",
        "user": "Vijay",
        "active": true
    }

Let’s now extract the JSON data from this config.json file.
	
    // main.go
    package main
    
    import (
        "encoding/json"
        "io/ioutil"
        "log"
    )
    
    // The data struct for the decoded data
    // Notice that all fields must be exportable!
    type Data struct {
        Origin string
        User   string
        Active bool
    }
    
    func main() {
        // Let's first read the `config.json` file
        content, err := ioutil.ReadFile("./config.json")
        if err != nil {
            log.Fatal("Error when opening file: ", err)
        }
    
        // Now let's unmarshall the data into `payload`
        var payload Data
        err = json.Unmarshal(content, &payload)
        if err != nil {
            log.Fatal("Error during Unmarshal(): ", err)
        }
    
        // Let's print the unmarshalled data!
        log.Printf("origin: %s\n", payload.Origin)
        log.Printf("user: %s\n", payload.User)
        log.Printf("status: %t\n", payload.Active)
    }

You should get the below output, after creating config.json.

### Sample Output

    2021/02/07 16:53:53 origin: golangdocs.com
    2021/02/07 16:53:53 user: Vijay
    2021/02/07 16:53:53 status: true

Seems straightforward, but you must be a bit careful about one thing, if you’re a newcomer to go.


Golang has a concept of “exported” fields in struct datatypes and functions, so this essentially means that these exported fields are the ones which will be visible across different packages. Since the json unmarshal function is external, it can only see exportable fields.


To make a field exportable, just ensure that you capitalize it! That’s why it’s Origin, User and Active, as opposed to origin, user and active.

### Reading Unstructured Data from JSON Files

If the contents of our config.json file keep changing regularly, it is practically impossible to keep track of the changes by modifying the struct fields again and again.


To simplify this, we can use the concept of encoding arbitrary data as an interface. We can replicate the JSON structure by visualizing it as a key-value map.


Here, the key will be a string, and the value can be any interface{}.


So we can simply modify the Data struct into a map[string]interface{}!

    // main.go
    package main
    
    import (
        "encoding/json"
        "io/ioutil"
        "log"
    )
    
    func main() {
        // Let's first read the `config.json` file
        content, err := ioutil.ReadFile("./config.json")
        if err != nil {
            log.Fatal("Error when opening file: ", err)
        }
    
        // Now let's unmarshall the data into `payload`
        var payload map[string]interface{}
        err = json.Unmarshal(content, &payload)
        if err != nil {
            log.Fatal("Error during Unmarshal(): ", err)
        }
    
        // Let's print the unmarshalled data!
        log.Printf("origin: %s\n", payload["origin"])
        log.Printf("user: %s\n", payload["user"])
        log.Printf("status: %t\n", payload["active"])
    }

Notice now that we can store arbitrary data easily, due to the interface{} map!

