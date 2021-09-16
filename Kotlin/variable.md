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
- 변수에 null 값을 넣으려면 타입명 뒤에 ?를 붙이고 null값을 넣어야 한다.
```kotlin
var temp: String = "ABCD"
temp = null // 문법 오류
```   
```kotlin
fun main() {
    var a : String? = "test"
    print(a.length)
```

- return type 에 ? 가 붙으면, return type 이 null 도 될 수 있다는 의미이다.
 ```kotlin
var temp: String? = "ABCD"
temp = null
```
---
a가 null이 가능한 String 타입일 때, 그대로 출력하면 오류가 발생한다.

 <b>그 이유는</b>, a가 null 일수도 있기에 안전하지 않기 때문이다.   

<b>따라서</b>, null 이 아닐때만 호출 할 수 있도록 조건문을 사용해야 한다.

```kotlin
fun main() {
    var a : String? = "test"
    print(a.length) //오류 발생
    if(a != null) print(a.length) // 4 출력
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
```kotlin
fun main() {

    val test = "Test.Kotlin.String"

    //test 의 길이
    println(test.length)

    //소문자로 변환
    println(test.toLowerCase())
    //대문자로 변환
    println(test.toUpperCase())

    //.을 기준으로 자름
    val test2 = test.split(".")
    println(test2)

    //그냥 합쳐짐
    println(test2.joinToString())
    //-를 넣어 합쳐짐
    println(test2.joinToString("-"))

    // 일부분만 사용 가능
    // 5번쨰 값부터 10번째 까지
    println(test.substring(5..10))
}
```
### output
```kotlin
18
test.kotlin.string
TEST.KOTLIN.STRING
[Test, Kotlin, String]
Test, Kotlin, String
Test-Kotlin-String
Kotlin
```

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