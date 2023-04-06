# Directory
```
<home>/
|-- greetings/
|-- hello\
```
gretting.go
```
package greetings

import "fmt"

func Hello(name string) string {
  message := fmt.Sprintf("hi, %v. Welcome!", name)
  return message
}
```
Enable dependency tracking
```
$ go mod init example.com/hello
```
hello.go
```
package main

import (
  "fmt"
  "example.com/greetings"
)

func main() {
  message := greetings.Hello("Gladys")
  fmt.Println(message)
}
```
redirect go tools from its module path
```
$ go mod edit -replace example.com/greetings=../greetings
```
dependency 동기화 및 미추적 dependency 추가
```
$ go mod tidy
```
