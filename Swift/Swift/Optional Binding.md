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