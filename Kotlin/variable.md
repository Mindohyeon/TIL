# 변수

## var

- 읽기/쓰기가 모두 가능한 변수
- 할당 후 변경이 가능하다.

```kotlin
var a : Int = 10 // a = 10
var b : Char = 'a' // b = 'a'
```

## val

- 읽기만 가능한 변수
- 할당 후 변경이 불가능하다.

```kotlin           
val b : Int = 10
b = 30  //오류 발생
```

## null

- 코틀린의 기본 변수는 null값을 가질 수 없다.
```kotlin
var temp: String = "ABCD"
temp = null // 문법 오류
```

- return type 에 ? 가 붙으면, return type 이 null 이 될 수 있다는 의미이다.
 ```kotlin
var temp: String? = "ABCD"
temp = null
```

## type

- String
- Char
- Int
- Boolean
- Byte
- Short
- Long
- Float
- Double
- List
- Set
- Map

### String

문자열 데이터

### Char

단일 문자

### Int

4byte 정수

### Boolean

true or false

### Byte

1byte 정수

### Short 

2byte 정수

### Long

8byte 정수

### Float

4byte 실수

### Double

8byte 실수

### List 
값을 요소로 저장하는 컬렉션

### Set

중복 없이 고유한 값의 요소를 저장하는 컬렉션

### Map

키와 값의 쌍으로 요소를 저장하는 컬렉션