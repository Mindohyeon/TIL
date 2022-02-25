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


## Opaque Type & Generics
- 불투명한 타입은 제네릭과 관련이 있다. 불투명한 타입은 보통 reserve generic type 이라고 불리기도 한다.
- 제네릭 타입의 placeholder 를 사용하면 함수 호출자가 placeholder 의 구체적인 형식을 결정한다.
- 불투명한 타입을 사용하면 구현에서 구체적인 유형을 결정한다.

##### SwiftUI 는 불투명한 리턴 타입이라고 불리는 개념에 크게 의존한다. view 를 작성할 때마다 작동하는 것을 볼 수 있고, 이 내용은 "View" 프로토콜을 준수하는 하나의 특정 타입이지만 이것이 무엇인지는 말하지 않는다는 것을 의미한다.

-> 개발자의 의도를 불투명하게 하는 유지하는 것이 생산성에 쉽다.