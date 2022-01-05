# left VS leading / right VS trailing

일단 leading 과 trailing 을 사용하는 이유는 localized(현지화) 때문이다.
이와 같이 설정하면 RTL(right-to-left) 순서로 읽는 지역에서는 화면이 거꾸로(flip)되어 표시된다.

= leading, trailing 으로 하면 오른쪽에서 왼쪽으로 읽는 지역에서 flip 된 UI 가 나온다!

반면에 left, right 를 사용하면 flip 되지 않는다.

- text 를 보여줄 때에는 <b>leading, trailing</b> 을 사용하고, 그림이나 지도와 같이 이미지가 보이는 view 를 보여줄 때에는 <b>left , right</b> 를 사용하는 게 낫다.