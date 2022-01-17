# Codebase 로 UI 만들기


## SnapKit
SnapKit 이란 Codebase 로 UI를 만들 때 더 쉽게 할 수 있게 해주는 라이브러리이다.

<b>SnapKit 을 사용할 때는 해석하는 방향이 중요하다.</b>
- 순차적으로 해석한다. 상단을 box1의 하단과 동일하게 offset은 30만큼
```swift
$0.top.equalTo(box1.snp.bottom).offset(30)
```