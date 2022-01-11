# Enum
Enum(enumeration) 이라는 셈, 열거, 목록 이라는 영단어의 앞 부분만 따서 만든 예약어이다.

관련이 있는 상수들의 집합이다. <b>어떤 클래스가 상수만으로 이루어져 있다면 반드시 class 로 선언할 필요는 없다. </b>

이럴때에는 class 로 선언된 부분에 enum 이라고 선언하면 이 객체는 상수의 집합이다 라는 것을 명시적으로 나타낸다.

swift 의 Enum 은 1급 객체이다.  

- 계산 프로퍼티를 가질 수 있다.
- 인스턴스 메서드를 가질 수 있다.
- 생성자를 가질 수 있다.
- extension 을 적용할 수 있다.
- 프로토콜을 채택할 수 있다.

<b>저장 프로퍼티는 가질 수 없고, enum 은 값 타입이라는 점에서 클래스와는 분명한 차이가 있다.</b>

```swift
enum : Name : Int {
    case name1
    case name2
    case name3
}
```

아래처럼 한 줄로 나열할 수도 있다.

```swift
enum : Name : Int {
    case name1 , name2 , name3
}
```

## Raw Values
열거형의 case 는 모두 독립적인 값이지만 내부에 또 다른 값을 저장할 수 있는데 이것을 <b>원시값(Raw Values)</b> 이라고 한다.

열거형을 정의할 때 <b>원시값 저장은 필수가 아니다.</b>

직접 만든 열거형에 원시값을 저장하는 경우는 상대적으로 적다. 그러나 개발할 때 주로 사용하는 프레임워크에는 정수형 원시값이 저장된 열거형으로 사용하는 경우가 상당히 많다.

```swift
enum : Name : Int {
    case name4
    case name5
    case name6
}
```
- 열거형 이름 뒤에 원시값의 타입을 지정해준다. 
- case 마다 원시값을 할당할 수 있다.
- 원시값 타입으로 올 수 있는 것은 <b>Number Type , String Type , Character Type</b> 으로 제한된다.

<b>선언 시점에 선언한 원시값은 나중에 바꿀 수 없다.</b> 원시값을 지정하는 부분은 생략할 수 있고, 생략할 경우 자료형 마다 각각 원시값 규칙이 존재한다.

### Number Type

```swift
enum Month: Int {
  case january = 1
  case february //2
  case march //3

  func simpleDescription() -> String {
    switch self {
    case .january:
      return "1월"
    case .february:
      return "2월"
    case .march:
      return "3월"

    }
  }
}

let march = Month.march
print(march.simpleDescription()) // 3월
print(march.rawValue)            // 3
```

원시값 할당을 생략하면 0부터 1씩 증가하며 차례대로 할당된다.
```swift
Month.january.rawValue //1
Month.february.rawValue //2
Month.march.rawValue //3

```
january 에만 1을 직접 할당했기 때문에 1부터 1씩 증가한다.   
증가될 때 기준값은 이전 case 이기 때문이다.

### enum 생성자
```swift
Month(rawValue : 3) //march
// 동일한 rawValue 를 가진 march 가 생성된다.

Month(rawValue : 100) //nil
// 이런 경우에는 nil 을 반환한다.
//  nil 을 return 할 수 있기 때문에 생성자의 리턴형은 옵셔널이다.
```

### String Type

```swift
enum Weekday : String {
    case sunday
    case monday
    case tuesday
    case wednesday
    case thursday
    case friday
    case saturday
}

Weekday.sunday.rawValue // "sunday"
```

원시값의 자료형을 String 으로 하고 원시값 할당을 생략하면 case 이름과 동일한 문자열의 원시값이 저장된다. 직접 할당할 수도 있다. 

### Character Type

Character Type 의 경우에는 항상 원시값을 직접 할당해주어야 한다. 

```swift
enum ch : Character {
    case first = "a"
    case second = "b"
}
```

직접 할당해주지 않으면 <b>컴파일 에러</b>가 난다.


### 원시값의 한계
- 모든 케이스가 동일한 형식을 사용한다.
- case 당 하나의 값만 저장할 수 있다.
- 원시값 문자열에 숫자가 포함되어 있을 경우에 숫자만 사용하려면 따로 추출해야하는 번거로움이 있다.

---

## 옵셔널은 Enum 으로 구현되어 있다.

```swift
public enum Optianal<Wrapped> {
  case none
  case some(Wrapped)
}
```

이것이 옵셔널이 '값' 과 '없는 값' 을 가지고 있는 이유이다.

또한 옵셔널은 Enum 이기 때문에 아래와 같이 구현할 수 있다.

```swift
let age : Int? = 22

switch age {
  case .none :
    print("나이 정보가 없습니다.")

  case .some(let x) where x < 20 : 
    print("청소년")

  case .som(let x) where x >= 20 : 
    print("성인")

  default : 
  print("사람")
}
```