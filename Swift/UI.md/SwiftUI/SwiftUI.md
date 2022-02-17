# SwiftUI
SwiftUI 란 모든 Apple 플랫폼에 대한 사용자 인터페이스를 선언하는 현대적인 방법이다. 빠르고 아름답게 역동적인 앱을 만들 수 있다.

## 장점
- 간단하고 깔끔한 코드 작성 가능
- 실시간 미리보기(live preview) 제공

## 단점
- iOS 13, Xcode11 이후 버전만 지원

## 구조 설명
SwiftUI 앱 라이프 사이클을 사용하는 앱은 <b>App 프로토콜</b>을 준수해야 하고, ```body``` 프로퍼티는 하나 이상의 ```scene``` 을 반환한다. ```@main``` 은 앱의 진입점을 가리키는 <b>attribute identifier</b> 이다. 

SwiftUI View 를 커스터마이징 하기 위해서는 ```modifiers``` 라는 메서드를 호출해야 한다. 이 modifiers 는 뷰를 랩핑해서 디스플레이나 다른 속성들을 변경한다. <b>각각의 modifiers 는 새로운 View를 반환하기 때문에 여러 modifiers 를 수직으로 쌓듯이 연결하는게 일반적이다.</b>

```swift
struct ContentView: View {
    var body: some View {
        Text("Turtle Rock")
            .font(.body) // modifier
            .fontWeight(.medium) // modifier
            .foregroundColor(.green) // modifier
    }
}
```

위 코드처럼 .font(.body), fontWeight(.medium) 와 같은 것들이 다 modifiers 다.

## ContentView
이 파일에서 오른쪽 빈 여백을 통해 Preview 를 볼 수 있다.
Command 를 누른 상태에서 Preview 의 TextView 를 클릭하면 SwiftUI Inspector 를 통해 스토리보드의 Attribute Inspector 와 마찬가지로 Text 내용이나 폰트, 패딩 등을 여러가지 설정할 수 있다. preview 에서 설정한 내용은 바로바로 코드에 반영된다.