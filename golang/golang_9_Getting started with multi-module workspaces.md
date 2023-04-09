```
$ cd
$ mkdir workspace
$ cd workspace
$ mkdir hello
$ cd hello
$ go mod init example.com/hello
```
Add a dependency
```
$ go get golang.org/x/example
```

hello.go
```
package main

import (
  "fmt"
  "golang.org/x/example/stringutil"
)

func main() {
  fmt.Println(stringutil.Reverse("Hello"))
}
```
run the hello
```
$ go run example.com/hello
```
Initialize the workspace
```
$ go work init ./hello
```
Run the program in the workspace directory
```
go run example.com/hello
```
