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

위 코드에 있는 backward 함수를 클로저 표현식 구문으로 바꾼다면

```swift
reversedNames = names.sorted(by : { (s1 : String, s2 : String) -> Bool in
    return s1 > s2})
```

따로 작성했던 backward 함수를 매개변수를 넣는 () 안에 넣었다.   
위 코드처럼 짧은 코드라면 한 줄로 쓸 수 있다.

```swift
reversedNames = names.sorted(by : { (s1 : String, s2 : String) -> Bool in return s1 > s2})
```

sorted(by:) 메서드는 매개변수로 함수 타입을 받기 때문에 결과적으로 반환 타입을 유추할 수 있다.   

즉, String Array 를 정렬할 것이기 때문에 (String, String) -> Bool 이라는 함수 타입을 받을 것이란 것을 유추할 수 있기 때문에, 굳이 써주지 않아도 된다.

```swift
reversedNames = names.sorted(by : { (s1,s2 in return s1 > s2)})
```

코드는 더 짧아졌지만, 이렇게 하면 코드를 이해할 때 어려울 수 있기 떄문에 아까처럼 타입을 명시하는 방법이 더 좋을 수도 있다.

s1 > s2 의 결과가 Bool 이기 때문에 Bool 값을 반환한다고 유추할 수 있기 때문에 return 도 생략할 수 있다.

```swift
reversedNames = names.sorted(by : { (s1,s2 in s1 > s2)})
```

#### Shortand Argument Names
Swift 는 인라인 클로저에서 인수 이름을 간단하게 사용하는 방법을 제공한다.
순서에 따라 $0,$1 와 같이 사용된다. swift 가 이를 어떤 인수인지 유추하여 잘 수행한다. 여기서 in 키워드마저 생략해버리면

```swift 
reversedNames = names.sorted(by : { $0 > $1})
```

