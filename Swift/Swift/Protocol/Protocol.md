# Protocol
특정 역할을 하기 위한 메서드, 프로퍼티, 기타 요구사항 등의 청사진이다.

## Protocol 사용
- 프로토콜은 정의를 하고 제시를 할 뿐 스스로 <b>기능을 구현하지는 않는다. (조건만 정의한다.)</b>
- 클래스, 구조체, 열거형은 프로토콜을 채택해서 특정 기능을 실행하기 위한 프로토콜의 요구사항을 실제로 구현할 수 있다.
- 하나의 타입으로 사용되기 때문에 아래와 같이 타입 사용이 허용되는 모든 곳에 프로토콜을 사용할 수 있다.

> - 함수, 메서드, 이니셜라이저의 파라미터 타입 혹은 리턴 타입
> - 상수, 변수, 프로퍼티의 타입
> - 배열, 딕셔너리의 원소 타입

### 기본 형태
```swift
protocol 프로토콜이름 {
    //프로토콜 정의
}
```

- 클래스, 구조체, 열거형 등에서 프로토콜을 채택하려면 이름 뒤에 콜론을 붙이고 채택할 프로토콜 이름을 쉼표로 구분해서 명시한다.

```swift
struct A : AProtocol {
    //구조체 정의
}
```
- subClass 의 경우에는 <b>superClass</b> 를 가장 앞에 명시한다.

```swift
class A : superClass : AProtocol {
    //클래스 정의
}
```

## Protocol 생성
- 프로토콜 프로퍼티
- 프로토콜 메서드

### 프로토콜 프로퍼티
- 연산 프로퍼티만 가능하고, 이름과 타입, ```get, set``` 의 유무만 명시한다.
- <b>항상 var 로 선언해야 한다.</b>

```swift
protocol Student {
    var name : String { get set }
    var number : Int { get }
    static var score : Double { get }
}
```

### 프로토콜 메서드
- <b>인스턴스 메서드</b>와 <b>타입 메서드</b>를 정의할 수 있다.
- <b>메서드 파라미터의 기본 값은 프로토콜 안에서 사용할 수 없다.</b>
- 구현부는 뺴고 그대로 작성한다.
- 정의할 때 <b>함수명과 반환값을 지정</b>할 수 있고, ```{}``` 는 적지 않는다.
- ```mutating``` 키워드를 사용해 <b>인스턴스에서 변경 가능하다는 것을 표시할 수 있다. (값 타입에서만 가능하다.)</b>

```swift
protocol Person {
    func breathing()
    func sleeping(time : Int) -> Bool
    static unc walking()
    mutating func walking()
} 
```

### initializer Requirements
프로토콜에서는 이니셜라이즈저도 정의할 수 있다.

```swift
protocol AProtocol {
    init(AParameter : Int)
}
```

프로토콜에서 특정 이니셜라이저가 필요하다고 명시해줬기 때문에 구현할 때에는 해당 이니셜라이저에 ```required``` 키워드를 붙여줘야 한다.

```swift
class AClass : AProtocol {
    required init(AParameter : Int) {
        //구현
    }
}
```

SuperClass 의 이니셜라이저를 SubClass 에 상속하는 경우 <b>SubClass 의 이니셜라이저 앞에 ```required``` 키워드와 ```override``` 키워드를 붙여줘야 한다.</b>

```swift
protocol AProtocol {
    init()
}

class ASuperClass {

}

class BSubClass : ASuperClass, AProtocol {
    required override init() {
        //구현
    }
}
```