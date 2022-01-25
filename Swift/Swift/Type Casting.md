# Type Castiong 이란?

인스턴스의 타입을 확인 하거나, 해당 인스턴스를 슈퍼 클래나 하위 클래스로 취급하는 방법이다.

Swift의 타입 캐스팅은 <b>is</b> 나 <b>as</b>연산자로 구현한다.

## is

```swift
표현식 is Type
```

타입을 체크하는 연산자로, 런타임 시점에서 실제 체크가 이루어진다. 표현식이 Type과 <b>동일하거나</b>, 표현식이 Type의 <b>서브 클래스</b>인 경우 = <b>true</b>
이 외에는 = <b>false</b>

반환값은 Bool 형이다.

#### 동일한 타입인지 확인
```swift
let test : Character = "A"

test is Character //true
test is String //false

let bool : Bool = true

bool is Bool //true
bool is Character //fasle
```

#### 표현식이 Type 의 서브클래스인지 확인
```swift
class Human{}
class Teacher : Human {}

let teacher : Teacher = .init()
teacher is Teacher //true
teacher is Human //true

```