# GO Start

1. 홈디렉터리 진입 $ cd
2. hello 디렉토리 생성 $ mkdir hello $ cd hello
3. go 언어는 dependency tracking을 위해 모듈 생성 module path는 통상적으로 소스코드가 존재하는 곳으로 지정
   $ go mod init example/hello
4. hello.go 파일 생성 후 아래 코드 복사  
```
package main // functions의 group형성 방법 동일한 디렉토리에 있는 모든 파일로 구성

import "fmt" // go 설치 시 기본 포함 라이브러리, text 출력, console 출력 담당

func main() {
   fmt.Println("Hello, World!") // 콘솔에 메세지 출력
}
```
5. 코드 실행 후 확인 $ go run .
6. [external package site](https://pkg.go.dev/)

