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

## as
```swift
표현식 as  (변환 할) Type
표현식 as? (변환 할) Type
표현식 as! (변환 할) Type
```

- 표현식의 타입이 변환할 Type과 호환된다면,  변환할 Type으로 캐스팅된 인스턴스를 return 한다.
- 상속 관계인 업캐스팅과 다운캐스팅에 사용한다.
- Any 와 AnyObject 타입을 사용할 경우, 상속 관계가 아니어도 예외적으로 사용할 수 있다.

---

### 형변환
Int(data), String(data) 등을 얘기한다.

만약,
```swift
solution(_ s: String) -> Int {
    return Int(s)
}

solution("1234")
```

위 같은 상황에서 String 타입의 s 를 ㅑㅜㅅ