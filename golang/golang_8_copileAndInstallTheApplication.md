$ go run은 코드가 자주 변경된다면 유용한 커맨드이지만 바이너리 파일을 생성하지는 않는다.
코드를 실행가능한 파일로 컴파일
```
$ go build
```
현재 패키지 설치, 즉 go 명령이 설치할 위치 찾기
```
$ go list -f '{{.Target}}'
```

명령의 출력은 /home/gopher/bin/hello와 같이 나타날 수 있습니다. 이는 바이너리가 /home/gopher/bin에 설치된다는 것을 의미합니다. 다음 단계에서 이 설치 디렉토리가 필요합니다.

```
$ export PATH=$PATH:/path/to/your/install/directory
```

shell안에 $HOME/bin같은 경로가 이미 있다면 대안이 존재한다.
```
$ go env -w GOBIN=/path/to/your/bin
```
or
```
$ go env -w GOBIN=C:\path\to\your\bin
```
컴파일 및 install 진행
```
$ go install
```
파일 이름으로 간단히 실행
```
$ hello
```
