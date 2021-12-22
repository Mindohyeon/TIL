# Swift 의 중요한 것들을 적습니다.😃

- Swift 는 문자열 리터럴을 여러 줄로 나눌 수 없다.

윈도우가 라인보다 좁으면 편집기는 표시 목적으로 랑니을 줄바꿈 할 수 있다.   
하지만 실제로 줄을 바꿔 문자열 리터럴을 넣을 수는 없다.   

```swift
let s = "Hello
 World"
```
이렇게 선언 시 ```Unterminated string literal```    오류가 발생한다.
