# Swift 의 중요한 것들을 적습니다.😃

## 1.  Swift 는 문자열 리터럴을 여러 줄로 나눌 수 없다.

윈도우가 라인보다 좁으면 편집기는 표시 목적으로 랑니을 줄바꿈 할 수 있다.   
하지만 실제로 줄을 바꿔 문자열 리터럴을 넣을 수는 없다.   

```swift
let s = "Hello
 World"
```
이렇게 선언 시 ```Unterminated string literal```    오류가 발생한다.

## 2. Swift 에서의 Singleton 구현?

여러가지 방법이 있지만 , 가장 쉬운 방법은 ```init()``` 메서드를 사용하는 것이다.

```swift
class UserInfo {
    static let shared = UserInfo()

    var id : String?
    var name : String?
    var password : String?

    private init() {}
}
```
혹시라도 ```init()``` 메서드를 호출해 <b>```instance``` 를 또 생성하는 것을 막기 위해,    
init() 메서드의 접근 제어자를 ```private``` 로 지정</b>해주면 된다.

