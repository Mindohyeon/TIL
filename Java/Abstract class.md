# Abstract Class 란?
일반 class 는 new 연산자를 사용해 인스턴스를 생성할 수 있지만, <b>추상 클래스는 인스턴스를 생성할 수 없고 오직 상속을 통해 완성된 자식 클래스로 구현해서 인스턴스를 생성할 수 있다.</b>

메서드 본체를 완성하지 못한 메서드를 <b>추상 메서드(Abstract Method)</b> 라고 한다.
- 추상 메서드를 포함하는 클래스는 인스턴스를 생성할 수 없으므로 추상 클래스이다.
- 추상 크랠스는 보통 하나 이상의 추상 메서드를 포함하는데, 포함하지 않을 수도 있다.

### 사용
추상 클래스는 주로 상속 계층에서 자식 멤버(필드, 메서드)의 이름을 동일하는 데 사용된다.

<b>구현 클래스를 ㅁ나드는 부모 클래스로만 사용할 뿐 new 연산자로는 인스턴스를 생성하지 못한다.</b>

```java
추상 클래스 s = new 추상클래스(); // 추상클래스는 인스턴스를 생성하지 못한다.
```