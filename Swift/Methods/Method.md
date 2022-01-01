# Method

## Method 란?
- 함수는 독립적인 기능을 위한 것이고, 메서드는 <b>하나의 객체 내에 정의된 다른 메서드들과 상호 협력해 함수적인 기능을 한다.</b>
- 메서드는 <b>인스턴스 메서드</b>와 <b>타입 메서드</b>로 나뉜다.


## 인스턴스 메서드(Instance Method)
객체 타입이 만들어내는 인스턴스에 소속된 함수로써, 객체의 인스턴스에 대한 기능적인 측면을 제공한다.
- 객체 내부에서 선언된다는 점을 제외하고는 일반 함수와 선언하는 방식이 동일하다.

## 타입 메서드(Type Method)
인스턴스를 생성하지 않고, 객체 타입 자체에서 호출할 수 있는 메서드이다. 인스턴스 메서드는 객체 타입의 인스턴스에 대해 호출하는 것이지만, 타입 메서드는 <b>객체 자체에 대해 호출한다.</b>
- 타입 프로퍼티와 성질이 같다.
- 구조체 , 열거형, 클래스 모두 타입 메서드를 선언할 때에는 ```static``` 키워드를 사용한다.
- 하위 클래스에서 오버라이딩할 타입 메서드를 선언할 때에는 ```class``` 키워드를 사용한다.(클래스 타입에서만 사용 가능하다.)

## 외부로부터 이름 숨기기  
외부 파라미터 이름에 ```_``` 기호를 사용하면, 함수를 호출할 때 파라미터 이름을 생략할 수 있다.

```swift 
func add3(_ a : Int, _ b : Int) {
    pirnt("add3가 호출되었다. : \(a), \(b)")

}
add3(10,20)
```
