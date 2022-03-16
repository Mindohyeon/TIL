# SwiftUI 의 Error 모음

#### Return from initializer without initializing all stored properties
구조체의 모든 속성이 init 메서드에서 초기화되지 않은 경우에 발생한다.

```swift
var listData : [TodoListItem] = []

@State var isAddView : Bool

init() {
    for item in 0...15 {
        listData.append(.init(name: "item"))
    }
}
```

이렇게 있다고 가정한다면

isAddView 를 초기화해주지 않았기 때문에 에러가 발생한다.