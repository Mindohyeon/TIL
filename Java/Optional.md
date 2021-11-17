# Optional 이란?
Java에서는 Optional< T > 클래스를 사용해 NPE 를 방지할 수 있도록 도와준다.
Optional< T >는 <b>null 이 올 수 있는 값을 감싸는 Wrapper 클래스</b>이다.

- 참조해도 NPE 가 발생하지 않도록 도와준다.

### 정리
NPE 가 나지 않도록 도와주는 즉, <b>NPE 방지</b>

- 흔하게 볼 수 있는 NPE 방지 코드는 if문을 사용하여 값이 null 이 아닌 경우에 동작하게 한다.


if문 대신 Optional 클래스를 사용하면 코드를 효과적으로 줄일 수 있다.