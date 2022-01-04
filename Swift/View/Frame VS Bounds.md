# Frame VS Bounds

## Frame 이란?
<b>SuperView(상위 뷰) </b>안에서 View 의 위치와 크기를 나타낸다.   

<b>중요 :</b> 상위 뷰

상위 뷰로부터 얼만큼 떨어졌는지 나타낸다. padding 과 비슷하다.

## Bounds 란?
View 의 위치와 크기를 자신만의 좌표시스템 안에서 나타낸다.

<b>중요 : </b>자신만의 좌표시스템을 사용한다.

<b>상위 뷰와 아무런 상관이 없고</b> 자신이 기준이다.

---

### origin?
origin 은 위치를 나타낸다.
### size?
size 는 크기를 나타낸다.