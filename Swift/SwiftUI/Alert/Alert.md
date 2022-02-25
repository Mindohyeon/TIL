# Alert
SwiftUI 에서 Alert 는 UIKit 에서의 UIAlertView 와 동일하다.


### 기본코드
```swift
.alert(isPresented: $___) {
    Alert(title: Text(""), message: nil, dismissButton: .default(Text("")))
}
```

## 사용조건
- Alert 를 표시할지에 대한 여부를 결정하는 Bool binding(state)
- Alert 를 반환하는 closure

<b>SwiftUI 는 Bool 값이 상태이기 때문에 변경될 때마다 뷰를 새로 고친다.</b> 때문에 true 로 설정된 경우 Alert 가 표시된다. 만약 Alert 가 해제되면 Bool 값이 자동으로 false 로 변경된다.