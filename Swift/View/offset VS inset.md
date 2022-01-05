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