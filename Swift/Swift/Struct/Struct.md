# Struct (구조체) 란?
인스턴스의 값(Property)을 저장하거나 메서드를 제공하고 이를 캡슐화할 수 있는 swift 가 제공하는 타입이다.

클래스처럼 <b>인스턴스</b>를 만들어서 실제 작업에 쓸 수 있다.

```swift
struct Name {
    var name = "Min"

    func my_name() {
        pirnt("my name is \(name)")
    }
}

var Min : Name = Name()

print(Min.name)
Min.my_name()

Min.name = "Kim"
Min.my_name()
```

위 코드와 같이 class 와 코드가 거의 비슷하다. class 였던 것을 struct 로 바꾼 것 밖에 변경 사항이 없다. 이처럼 클래스와 구조체의 선언하고 사용하는 방법은 매우 비슷하다. 클래스와 같이 구조체 안의 변수를 <b>속성</b> , 함수를 <b>메서드</b>라고 한다.


