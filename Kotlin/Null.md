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

### ?.
- null safe operator
### ?:
- elvis operatior
### !!.
- non-null assertion operator
