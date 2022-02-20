# some
some 키워드는 return type 을 자동으로 빠르게 추론할 수 있는 스위치 기능이다.

- <b>불투명한 타입</b>이라는 것을 나타내는 some 키워드는 <b>computed property 혹음 함수의 구체적인 return type 을 숨기는 것이 가능하다.</b>

이를 통해서 <b>유연하고 간결하며 강력한 Swift 코드를 작성할 수 있다.</b>

```swift
struct FirstView : View {
    var body : some View {
        Text("Hello World!")
    }
}
```
- some 키워드는 computed property 인 body 안에 <b>불투명한 타입이 있음을 나타낸다.</b>
- body property에 구현되는 이 타입은 FirstView 를 사용하는 코드에 <b>노출되지 않고 비공개로 유지된다.</b>