# GO Start

1. 홈디렉터리 진입 $ cd
2. hello 디렉토리 생성 $ mkdir hello $ cd hello
3. go 언어는 dependency tracking을 위해 모듈 생성 module path는 통상적으로 소스코드가 존재하는 곳으로 지정
   $ go mod init example/hello
4. hello.go 파일 생성 후 아래 코드 복사
   ₩package main

import "fmt"

func main() {
fmt.Println("Hello, World!")
}₩
