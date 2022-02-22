# 다양한 Binding 방법

## annotations
- @State
- @Binding
- ObservableObject
- EnvironmentObject

### @State
뷰가 접근 가능하도록 값을 가지고 있는 프로퍼티 래퍼(Property Wrapper) 이다.
```Property Wrapper``` 란 쉽게 말해 사용자가 별도의 코딩 없이 어노테이션만 선언해도 뷰에서 수정이나 읽기가 가능하도록 <b>캡슐화</b>를 대신 해준다.

### '$' 키워드
$ 가 붙으면 프로퍼티 래퍼 자체를 받기 때문에 안에 있는 WrapperValue 자체를 변경할 수 있다.

- toggleOn -> Bool 값
- $toggleOn -> Binding<Bool>