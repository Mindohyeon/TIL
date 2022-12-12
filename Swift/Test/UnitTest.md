## 테스트코드 작성 중  'Thread 1: signal SIGABRT' 에러 발생

해당 문제는 reactor 에 isStubEnabled 를 true 로 바꿔주면 해결된다.

```swift
let reactor = ExampleReactor()
reactor.isStubEnabled = true // 이렇게 isStubEnabled를 true로 만들어주자

~~
```