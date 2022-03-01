# 다양한 Wrapper

- @State
- @Binding
- @ObservedObject
- @Environment

### @State
뷰가 접근 가능하도록 값을 가지고 있는 프로퍼티 래퍼(Property Wrapper) 이다.
```Property Wrapper``` 란 쉽게 말해 사용자가 별도의 코딩 없이 어노테이션만 선언해도 뷰에서 수정이나 읽기가 가능하도록 <b>캡슐화</b>를 대신 해준다.

해당 View 외부로는 사용할 수 없고, private 형태로 내부에서만 사용 가능하다.

두 개의 뷰가 하나의 State 를 참조해야 하는 경우가 생길 때 ```@Binding``` 을 사용할 수 있다.

State 는 Toggle 유뮤와 같은 UI 의 상태 값과 같은 아주 한정된 용도로만 사용하기를 권고하고 있는데 그 이유는 뷰 안에만 사용하는 메모리 공간이기 때문이다. 만약 뷰 밖의 클래스에서 사용하려면 ```ObservableObejct``` 를 사용 할 수 있다.

현재 뷰 UI 의 특징 상태를 저장하기 위해 만들어진 것이기 때문에 보통 Private 로 지정하여 사용한다.

### '$' 키워드
$ 가 붙으면 프로퍼티 래퍼 자체를 받기 때문에 안에 있는 WrapperValue 자체를 변경할 수 있다.

- toggleOn -> Bool 값
- $toggleOn -> Binding<Bool>

### @Binding
단순히 @Binding 어노테이션으로 선언하여 초기화할 때 State 값을 받는 것만으로 여러 개의 뷰가 동시에 State 값을 참조할 수 있다.


### @ObservedObject
별도의 클래스를 만들고 ObservableObject 프로토콜을 상속받으면 SwiftUI 에서 사용할 수 있다.

```swift
class countClass : ObservableObject {
    @Published var count : Int = 0
}
```

```swift
struct ContentView : View {

    @ObservedObject var countClass = countClass()

    var body : some View {
        Vstack {
            Text("self.countClass.count")

            Button("숫자 증가") {
                self.countClass.count += 1
            }
        }
    }
}
```

Published 어노테이션은 값이 변경되었을 때 바로 View 에게 즉각적으로 알려준다.

## @Environment
읽기 전용으로 특정 뷰에서 EnvironmentValues의 특정 요소를 읽어와 뷰 구성에 반영할 때 사용한다.



#### 참고

- https://seons-dev.tistory.com/169