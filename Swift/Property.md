# Property 란?
객체 지향 프로그래밍 언어에서 필드와 메소드 간 기능의 중간인 클래스 멤버의 특수한 유형이다.

Property 는 크게 5가지가 존재한다. 
- 저장 프로퍼티
- 지연 저장 프로퍼티
- 연산 프로퍼티
- 프로퍼티 감시자
- 타입 프로퍼티


## 저장 프로퍼티(Stored Properties)
가장 단순한 개념의 프로퍼티로써, 클래스 또는 구조체의 인스턴스와 연관된 값을 저장하는 프로퍼티이다.

> 구조체의 저장 프로퍼티가 옵셔널이 아니라도, 구조체는 저장 프로퍼티를 포함하는 이니셜라이즈를 자동으로 생성한다.

> 클래스의 저장 프로퍼티는 옵셔널이 아니라면 프로퍼티 기본값을 지정해주거나 사용자정의 이니셜라이즈를 통해 반드시 초기화해야한다. 그렇지 않으면 프로퍼티 초기값을 할당할 수 없기 때문에 인스턴스 생성이 불가능 하다.
```Swift
struct Stored {
    var x : Int  //저장 프로퍼티
    var y : Int  //저장 프로퍼티
}

//구조체는 기본적으로 저장 프로퍼티를 매개변수로 가지는 이니셜라이즈가 있다.
let point : stored = stored(x : 10, y : 10)

class Position {
    var pointer : stored //저장 프로퍼티(변수)
    let name : String //저장 프로퍼티(상수)
}

```

## 지연 저장 프로퍼티(Lazy Stored Properties)
```lazy``` 키워드를 사용하고, 호출이 있어야 값을 초기화 할 수 있다.

<b>상수는 인스턴스가 완전히 생성되기 전에 초기화</b> 되어야 하기 때문에 필요할 때 값을 할당하는 <b>지연 저장 프로퍼티에는 맞지 않다.</b> 따라서 ```var``` 키워드를 사용하여 변수로 정의한다.
- 주로 복잡한 클래스나 구조체를 구현할 때 사용된다.   

인스턴스를 초기화하면서 저장 프로퍼티로 쓰이는 인스턴스들이 한 번에 생성되거나 모든 저장 프로퍼티를 생성할 필요가 없다면 그때 지연 저장 프로퍼티를 사용하면 된다.

#### 효과
지연 저장 프로퍼티를 잘 사용하면 불필요한 성능 저하나 공간 낭비를 줄일 수 있다.     
```swift

struct Stored {
    var x : Int = 0
    var y : Int = 0
}

class Position {
    lazy var point : stored = stored()
    let name : String

    init(name : String) {
        self.name = name
    }
}
// position 이라는 객체는 생성됐지만 아직 Stored는 객체에 생성되지 않았다.
let position : Position = Position(name : "도현")

// 이 코드를 통해 point 프로프티로 처음 접근할 때 point 프로퍼티의 Stored 가 생성된다.
print(position.point)