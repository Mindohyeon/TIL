# Frame
뷰는 자신의 콘텐트와 자신이 속한 레이아웃에 따라 자동으로 크기가 조절된다. 하지만 frame 수정자를 사용하면 <b>뷰의 크기나 영역을 조절할 수 있다.</b>

```swift
.frame(width: 100, height: 100, aligment: .center)
```

프레임은 위와같이 가로, 세로, 정렬을 지정할 수 있고,

```swift
frame(minWidth: 1, idealWidth: 10, maxWidth: .infinity,
minHeight: 0, idealHeight: 10, maxHeight: .infinity, aligment: .center)
```
최소넓이, 이상적인 넓이, 최대 넓이, 최소 높이, 이상적인 높이, 최대 높이를 지정할 수 있다. (.infinity 는 말 그대로 무한대를 뜻한다.)

default frame 은 화면을 채울 때 화면의 <b>안전 영역(safe Area)을 준수한다.</b> 만일 안전 영역 밖까지 확장되도록 frame 을 구성하려면

뒤에 .edgesIgnoringSafeArea(.all)을 해주면 된다.

위의 조건 .all 뿐만 아니라,
- top, bottom, horizontal, vertical, leading, trailing 등이 있다.