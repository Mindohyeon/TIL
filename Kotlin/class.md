# Nested Class VS Inner Class
둘 다 클래스 내부에 또 다른 클래스를 정의하는 것을 의미한다.

## Nested Class (중첩 클래스)
형태만 내부에 존재할 뿐,   
<b>실질적으로는 서로 내용을 공유할 수 없는</b> 별개의 ```clss``` 이다.

## Inner Class (내부 클래스)
혼자서는 객체를 만들 수 없고 외부 클래스의 객체가 있어야만 생성과 사용이 가능하다.

- 외부 class 의 속성과 함수를 사용 가능.


# Data Class VS Enum Class

## Data Class
```Data``` 를 다루는 데에 최적화 된 ```class```

5가지 기능을 내부적으로 자동 생성해준다.

- <b>equals() 자동구현</b>

내용의 동일성 판단

- <b>hashcode() 자동구현</b>

객체 내용에서 고유한 코드 생성

- <b>toString() 자동구현</b>

포함된 속성을 보기쉽게 나타냄

- <b>copy() 자동구현</b>

객체를 복사하여 똑같으 내용의 새 객체를 만듦   
속성 변경도 가능

- <b>componentX() 자동구현</b>

속성을 순서대로 반환


