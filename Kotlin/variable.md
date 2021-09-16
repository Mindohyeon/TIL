# 변수

## var

- 읽기/쓰기가 모두 가능한 변수
- 할당 후 변경이 가능하다.   

```kotlin
var a : Int = 10 // a = 10
var b : Char = 'a' // b = 'a'
```
### lateinit var  

자료형만 선언해두고 나중에 초기화

#### 제한 사항
- 초기값을 할당하기 전까지 변수를 사용할 수 없다.(에러 발생)
- 기본 자료형에는 사용할 수 없다.(String 클래스에는 사용 가능)

####  lateinit 변수의 초기화 여부를 확인할 때

```::a.isInitialized``` 

초기화 되었는지 확인하여 오류를 막을 수 있다.
```kotlin
lateinit var text : String
```
### lazy

```kotlin
val a:Int by lazy {7} 
    ---
    println(a)   //이 시점에서 7 로 초기화 
```
코드의 실행시간을 최적화 할 수 있는 코드이다.

람다함수로 초기화가 진행되기 때문에 
```kotlin
val a : Int by lazy {
    println("initializing")
    7  // 이렇게 해도 어차피 값은 7
}
```
이렇게 적어도 값은 초기화 된다.


## val

- 읽기만 가능한 변수
- 할당 후 변경이 불가능하다.
- <b>할당된 객체를 바꿀 수 없지만, 객체 내부의 속성은 변경할 수 있다.</b>

```kotlin           
val b : Int = 10
b = 30  //오류 발생
```
## Const
생성 이후 값을 바꿀 수 없다.

의례적으로 대문자와 언더바(_)만 사용한다.
```kotlin
const val CONST_A = 1234
```
### 변수를 사용하지 않고 상수를 사용하는 이유는?
변수의 runtime 시 객체를 생성하는 데 시간이 더 소요되어 성능의 하락이 있기 때문이다.

- 늘 <b>고정적으로 사용할 값</b>은 상수를 통해 객체의 생성 없이 메모리 값을 고정하여 사용함으로써 <b>성능을 향상</b> 시킬 수 있다.

---

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
```kotlin
fun main() {
    val nullString : String? = null
    //empty = 비어있는 = null
    val emptyString = ""
    val blackString = " "
    val normalString = "O"

    println(nullString.isNullOrEmpty())
    println(emptyString.isNullOrEmpty())
    println(blackString.isNullOrEmpty())
    println(normalString.isNullOrEmpty())

    //줄바꿈
    println()

    println(nullString.isNullOrBlank())
    println(emptyString.isNullOrBlank())
    println(blackString.isNullOrBlank())
    println(normalString.isNullOrBlank())
}
```
### output
```kotlin
true
true
false
false

true
true
true
false
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