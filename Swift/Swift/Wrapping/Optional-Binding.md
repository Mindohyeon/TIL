# Optional Binding 이란?

옵셔널 변수의 값을 가져오는 방법이자, 옵셔널을 안전하게 처리하는 방법이다.

```swift
let num : Int? = 0
if let num = num {
    print(num)
} else {
    print("else")
}
// 0 출력
```

만약 num 이 nil이라면?
```swift
let num : Int? = nil
if let num = num {
    print(num)
} else {
    print("else")
}
//else 출력
```

보통 상수 이름과 OptionalExpression 의 이름은 같게 한다.

바인딩 한 상수는 else 블록 내부에서는 사용할 수 없고, else 블록 다음부터 사용가능하다.

```swift
var str: String? = "Hello"

guard let str = str else {
    //str error
    fatalError()
}
```

## Wrapping VS Unwrapping


#### wrapping
nil 을 사용하기 위해서는 Optional 을 사용해야 한다.
Optional로 선언된 자료형은 일반 자료형이 아닌 Optional 로 한 번 포장된 Opntional 자료형이다.
```?``` 키워드를 사용한다.

```swift
let a : Int? = nil
print(type(of : a))
//Optional<Int>
```

그냥 Int 가 아니라 Optional Int 자료형이다.

이렇게 포장지처럼 Optional 로 한 번 포장된 상태를 <b>Wrapping</b> 되었다고 하고, 이걸 벗기는 작업을 <b>Optional Unwrapping</b> 이라고 한다.


#### Unwrapping
```!``` 키워드를 사용한다.일단 쓰겠다는거다. 값이 있을수도 있고 없을 수도 있는데도 말이다.

만약 값이 존재하지 않는 Optional 값에 접근하려고 시도하면 런타임 에러가 발생한다. ```!``` 을 사용해서 Unwrapping 하기 위해서는 먼저 Optional 값이 nil 이 아니라는 것을 확실히 해야한다.

- ```!``` 또한 Optional 이기 때문에 초기화해주지 않으면 ```?``` 와 마찬가지로 nil 이 들어간다.




#### Optional Unwrapping 을 사용하기 위해서는 절대 Unwrapping 하고자 하는 변수가 nil 이면 안 된다.
```swift
let a : Int? = 5
print(a)
//Optional(5)

let b : Int? = nil
print(b)
nil

```

nil 이 지정된 변수를 Unwrapping 하려고 하면 <b>오류가 아니라 에러가 난다.</b>



#### 아래를 참고하자.   

[오류와 에러의 차이란 뭘까?](https://github.com/Mindohyeon/TIL/blob/main/Study/Simple/Error.md)