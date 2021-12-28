# Closure 란?
- 클로저는 사용자의 <b>코드 안에서 전달되어 사용할 수 있는 로직을 가진</b> 중괄호"{}" 로 구분된 <b>코드의 블럭</b>이며, <b>일급 객체의 역할</b>을 할 수 있다.
- <b>일급 객체는 전달 인자를 보낼 수 있고, 변수/상수 등으로 저장하거나 전달할 수 있으며, 함수의 반환 값이 될 수 있다.</b>
- <b>참조 타입</b>이다.
- <b>함수</b>는 클로저의 한 형태로, 이름이 있는 크로저이다.

### 표현 방식

```swift
{ (인자들) -> 반환타입 in
 로직 구현
}
```

### 기능
- 깔끔한 구문을 위해 최적화 기능이 있다.
- 구문에서 매개변수, 리턴 값 타입 유추를 할 수 있다.
- 클로저에서 암시적으로 반환 값을 반환할 수 있다.
- 매개변수의 인수 이름을 간단히 할 수 있다.
- Trailing closure syntax


## Closure Expressions (클로저 표현식)
Closure Expressions 는 간단하게 클로저를 작성하는 방법이다.

Swift 기본 라이브러리에서 제공하는 sorted(by:)메서드는 사용자가 정의한 값들을 Array 타입으로 반환해주는 클로저이다.

```swift
let name = ["B","A","C","D"]
```

위 코드와 같은 String Array 를 정렬해보자.

```swift
func backward(_ s1 : String, _ s2 : String) -> Bool {
    return s1 > s2
}
var reversedNames = names.sorted(by: backward)
// reversedNames = ["D","C","B","A"]
```