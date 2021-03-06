# Annotation
어노테이션이란 <b>클래스나 메서드, 변수에 @을 사용하는 것이다.</b>

### 사용 이유
어노테이션은 사전적 정의로 주석을 뜻한다. 주석과는 역할이 다르지만 , 주석처럼 달아 <b>특수한 의미 부여가 가능하고, 기능 주입이 가능하다.</b>

가장 큰 이유는 <b>프로그램에 추가 정보를 제공하는 메타 데이터를 위해서 사용한다.</b>


## @Override 어노테이션 기능
<b>자식 클래스에 여러 개의 메서드가 정의 되어 있을 경우</b>

해당 메소드가 부모 클래스에 있는 메서드를 Override 했다는 것을 명시적으로 알린다.
- 어떤 메서드가 부모 클래스로부터 Override 되었는지 쉽게 파악할 수 있다.

<b>컴파일러에게 문법 체크를 하도록 알린다.</b>

- override 를 제대로 했는지 확인할 수 있는 수단으로 사용될 수 있다.