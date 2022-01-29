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

## 구조체의 초기화
```swift
struct Name {
    var name : String

    func my_name() {
        print("my name is \(name)")
    }
}
var Min : Name = Name(name : "Min")

print(Min.name)
Min.my_name()
```
class 는 변수를 직접 초기화하지 않으려면 init() 메서드로 초기화 해줘야 하는데 구조체에서는 자동으로 초기화 코드를 만들어주기 때문에 쓰지 않아도 된다.

#### 에러
```swift
class Name {
    var name : String

    func my_name() {
        print("my name is \(name)")
    }
}
var Min : Name = Name(name : "Min")

print(Min.name)
Min.my_name()
```

### 구조체의 상속?
구조체는 상속이 불가능하다.

---

# Class VS Struct

### Class
- ```Call by Reference```(참조에 의한 호출) - 할당 또는 파라미터 전달시에 객체를 가리키고 있는 메모리 주소만 복사된다.   
- ```heap memory``` 영역에 할당 (속도가 느리다.)
- 상속이 가능하다.
- ```Codable``` 사용이 불가능하다.
- 런타임에 타입 캐스팅을 통해 클래스 인스턴스에 여러 동작이 가능하다.

### Struct
- ```Call by Value```(값에 의한 호출) - 할당 또는 파라미터 전달시에 value copy 가 일어난다.
- ```stack memory``` 영역에 할당 (속도가 빠르다.)
- 상속이 불가능하다. (Protocol 은 가능)
- ```Codable``` 프로토콜을 사용하여 JSON <-> Struct 변환 가능 (Swfit 4 이상만 가능)
- 항상 새로운 변수로 copy 가 일어나기 때문에 multi-thread 환경에서 공유변수로 인해 문제를 일으킬 확률이 적다.


## 어떤 상황에 써야할까?
- 상속이 필요하지 않고 모델의 사이즈가 그닥 크지 않다면 <b>struct</b> 사용
- JSON 필드와 1 : 1 mapping 되는 간단한 모델이 필요하다면 <b>struct</b> 사용
- 해당 모델을 serialize 해서 전송하거나 파일로 저장할 일이 있다면 <b>class</b> 사용
- 해당 모델이 Obj-C 에서도 사용되어야 한다면 <b>class</b> 사용