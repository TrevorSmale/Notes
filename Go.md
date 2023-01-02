# Go
## Personal Golang learning notes

# Creating a golang package

## 1. Initialize a new go module

'''go
go mod init github.com/trevorsmale/example
'''

## 2. Create repository, matching name of repo to name of module

## 3. Create initial go file with module functions

'''go
package mylogger

import "log"

func LogInfo(message string) {
    log.Printf("INFO - %v", message)
}
'''

## 4. Commit to github
