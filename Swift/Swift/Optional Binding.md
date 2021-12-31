# Optional Binding 이란?

옵셔널을 안전하게 처리하는 방법이다.

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
str 
```

## Wrapping VS Unwrapping
nil 을 사용하기 위해서는 Optional 을 사용해야 한다.
Optional로 선언된 자료형은 일반 자료형이 아닌 Optional 로 한 번 포장된 Opntional 자료형이다.

```swift
let a : Int? = nil
print(type(of : a))
//Optional<Int>
```

그냥 Int 가 아니라 Optional Int 자료형이다.

이렇게 포장지처럼 Optional 로 한 번 포장된 상태를 <b>Wrapping</b> 되었다고 하고, 이걸 벗기는 작업을 <b>Optional Unwrapping</b> 이라고 한다.

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