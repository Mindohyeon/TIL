# 메모리를 참조하는 방법 (Strong, Weak, Unowned)

## strong(강한 참조)
- 해당 인스턴스의 <b>소유권을 가진다.</b>
- 자신이 참조하는 인스턴스의 <b>retain count 를 증가시킨다.</b>
- 값 지정 시점에 <b>retain</b>이 되고 참조가 종료되는 시점에 <b>release</b> 된다.
- 선언할 때 아무것도 적어주지 않으면 <b>default 로 Strong 이다.</b>

```swift
var test = Test() // retain count 1 증가
test = nil //retain count 가 1 감소되어 0이 되면서 메모리가 해제된다.
```

## weak(약한 참조)
- 해당 인스턴스의 소유권을 <b>가지지 않고, 주소값만을 가지고 있는 포인터의 개념이다.</b>
- 자신이 참조하는 인스턴스의 retain count 를 <b>증가시키지 않는다. 또한 release 도 발생시키지 않는다.</b>
- 자신이 참조는 하지만 <b>Weak 메모리를 해제시킬 수 있는 권한은 다른 클래스에 있다.</b>
- 메모리가 해제될 경우에 자동으로 레퍼런스가 <b>nil로 초기화 해준다.</b>
- weak 속성을 사용하는 객체는 항상 <b>Optional 타입이어야 한다.</b>(해당 객체가 nil일 수도 있기 때문이다.)
- let 으로 선언할 수 없다.

> ARC 가 weak 참조를 nil 로 설정할 때, 프로퍼티 옵저버(프로퍼티 감시자)는 호출되지 않는다.

## unowned(미소유 참조/약한 참조)
- 해당 인스턴스의 <b>소유권을 가지지 않는다.</b>
- 자신이 참조하는 인스턴스의 retain count 를 <b>증가시키지 않는다.</b>
- nil 이 될 수 없기 때문에, <b>Optional 로 선언되면 안 된다.</b>

### *weak 와 unowned 의 차이
weak는 객체를 추적하면서 객체가 사라지게 되면 nil 로 바꿔준다.
하지만 unowned 는 객체가 사라지면 댕글링 포인터가 남는다.
이 ```댕글링 포인터```를 참조하면 <b>crash</b> 가 나기 때문에 <b>unowned는 사라지지 않을 거라고 보장되는 객체에만 설정해야 한다.</b>

<b>*댕글링 포인터(Dangling pointer)?</b> : 원래 바라보던 객체가 해제되면서 할당되지 않는 공간을 바라보는 포인터

### 어떤 상황에 쓸까?
- <b>strong</b> : 레퍼런스 카운트를 증가시켜 ARC 로 인한 메모리 해제를 피하고, 객체를 안전하게 사용하고자 할 때 쓴다.
- <b>weak</b>: 대표적으로 retain cycle에 의해 메모리가 누수되는 문제를 막기 위해 사용되며, delegate 패턴이 있다.
- <b>unowned</b> : 객체의 라이프사이클이 명확하고 개발자에 의해 제어 가능이 명확한 경우, weak Optional 타입 대신 사용하여 좀 더 간결한 코딩이 가능하다.

*<b>ARC(Automatic Reference Counting)?<b> : [ARC란?]("https://github.com/Mindohyeon/TIL/blob/main/Swift/ARC/ARC.md")

<b>*라이프 사이클(LifeCycle)?</b> : 객체의 생존 기간. 객체가 생성된 후부터 폐기될 때까지의 기간을 뜻한다.