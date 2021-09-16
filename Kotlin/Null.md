# Null

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
---
<b>null 상태로 속성이나 함수를 쓰려고 하면 null pointer exeption 발생</b>   
때문에 nullable 변수를 사용할때에는 if 문으로 null ceck를 하지 않으면 코드가 컴파일 되지 않는다.

## if 문 대신 null check 를 하는 방법
스코프 함수와 사용하면 더욱 편리하다.

### ?.
- null safe operator 
  
참조 연산자를 실행하기 전에 객체가 ```null``` 인지 확인하고 객체가 ```null```이라면
<b>뒤따라오는 구문을 실행하지 않는다.</b>

```kotlin
fun main() {
    val a : String? = null

    a?.run {
        println(toUpperCase())
        println(toLowerCase())
    }
}
```

### ?:
- elvis operator 

객체가 ```null``` 이 아니라면 그대로 사용하지만 ```null``` 일 경우엔 <b>연산자 우측 객체로 대체된다.</b>

### !!.
- non-null assertion operator

참조 연산자를 사용할 때 null 여부를 컴파일 시 확인하지 않게 하여 runtime 때 ```null pointer exeption``` 이 나도록 <b>의도적으로 방치한다.</b>

```kotlin
```

