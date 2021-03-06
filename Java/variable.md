# Variable (변수)


## 변수의 명명 규칙
- 대소문자를 구분한다.
- 길이에 제한이 없다.
- 변수명에는 예약어가 올 수 없다.
- 숫자로 시작할 수 없다.
- 특수문자는 _ 와 &만 가능하다.
- 상수는 모두 대문자만 가능하다.

## 약속
- 첫 번째 문자는 소문자인 명사로 정한다.
- 뜻이 있는 단어를 사용한다.
- 여러 단어로 구성된 이름의 경우는 두 번째 단어의 첫 글자는 대문자로 표기한다.
- _ 는 사용하지 않는다.

## 자료형

### 기본 자료형의 기본값 (Primitive Type)
바로 초기화가 가능하다.

- byte = 0
- short = 0
- int = 0
- long = 0L
- float = 0.0f
- double = 0.0d
- char = '\u0000'
- boolean = false

타입|할당되는 메모리 크기|기본값|
|---|--------------------|------|
blooean|1 byte|false|
byte|1 byte|0|
short|2 byte|0|
<b>int(기본)</b>|<b>4 byte</b>|<b>0</b>|
long|8 byte|0L|
float|4 byte|0.0F|
<b>double(기본)</b>|<b>8 byte</b>|<b>0.0</b>|
char|2 byte|'\u0000'|





위를 제외하고는 모두 참조 자료형이라고 봐도 무방하다.

### 참조 자료형 (Reference Type)
- <b>String과 같은 클래스 타입, 배열 , 열거 , 인터페이스</b>

기본값은 모두 <b>Null</b> 이다. 할당되는 메모리는 모두 <b>4 byte (객체의 주소값)</b>이다.

문법상으론 오류가 없지만 실행시 에러가 나는 runtime error 가 발생한다. 객체나 배열을 Null  값으로 받으면 ```NullPointerException``` 이 발생하므로 <b>변수값을 넣어줘야 한다.</b>

<b>new</b> 를 사용해서 초기화 한다.

<b>유일하게 String 은 new 없이도 객체를 생성할 수 있는 참조 자료형이다.</b>
```java
String name = "java";
```
대부분의 개발자는 이런 식으로 초기화한다.
```java
String name = new ("java");
```
하지만 이런식으로 정의해도 무관하다.