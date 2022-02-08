# 메모리를 참조하는 방법 (Strong, Weak, Unowned)

## Strong(강한 참조)
- 해당 인스턴스의 <b>소유권을 가진다.</b>
- 자신이 참조하는 인스턴스의 <b>retain count 를 증가시킨다.</b>
- 값 지정 시점에 <b>retain</b>이 되고 참조가 종료되는 시점에 <b>release</b> 된다.
- 선언할 때 아무것도 적어주지 않으면 <b>default 로 Strong 이다.</b>

```swift
var test = Test() // retain count 1 증가
test = nil //retain count 가 1 감소되어 0이 되면서 메모리가 해제된다.
```

## Weak(약한 참조)
- 해당 인스턴스의 소유권을 <b>가지지 않고, 주소값만을 가지고 있는 포인터의 개념이다.</b>
- 자신이 참조하는 인스턴스의 retain count 를 <b>증가시키지 않는다. 또한 release 도 발생시키지 않는다.</b>
- 자신이 참조는 하지만 <b>Weak 메모리를 해제시킬 수 있는 권한은 다른 클래스에 있다.</b>
- 메모리가 해제될 경우에 자동으로 레퍼런스가 <b>nil로 초기화 해준다.</b>
- Weak 속성을 사용하는 객체는 항상 <b>Optional 타입이어야 한다.</b>(해당 객체가 nil일 수도 있기 때문이다.)