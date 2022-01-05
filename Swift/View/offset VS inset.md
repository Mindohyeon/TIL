# offset VS inset

## offset 을 사용했을 때
```swift
box.snp.makeConstraints {
    $0.top.left.equalToSuperview().offset(50)
    $0.bottom.right.equalToSuperview().offset(-50)
}
```

### offset 의 공식
현재 뷰 constraint = 슈퍼뷰 constraint + offset 값   

따라서 bottom 과 right 는 마이너스 부호를 갖게 된다.   
프로그래밍계에서의 xy 좌표계에 의해서 정해진다.

## inset 을 사용했을 때
```swift
box.snp.makeConstraints {
    $0.top.left.bottom.right.equalToSuperview().inset(50)
}
```
이렇게 주면 offset 과 결과가 동일하게 나온다.

inset 의 경우에는 UIEdgeInsets 를 주었다고 생각하면 된다.

```swift
box.snp.makeConstraints {
    $0.top.left.bottom.right.equalToSuperview()
    .inset(UIEdgeInsets(top : 50, left : 50, bottom : 50, right : 50))
}
```

bottom 과 right 의 좌표값이 음수가 아니고 <b>양수</b>이다.

상하좌우가 같은 값이라면 아래의 코드처럼 깔끔하게 작성할 수 있다.
```swift
box.snp.makeConstraints {
    $0.edges.equalToSuperview().inset(50)
}
```