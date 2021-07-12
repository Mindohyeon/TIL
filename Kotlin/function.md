# 함수

- Java 에서의 void는 Kotlin 에서 Unit이다.
### 선언 방법
- fun 함수명(변수명 : 변수 타입): 리턴타입

#### return 값이 있는 함수
```kotlin
fun main(){
    println(add(4, 5))  //9출력
}

fun add(a : Int, b : Int) : Int{
    return a + b
}
```  
return 값이 있는 함수일 경우 return type 필요
#### return 값이 없는 함수

```kotlin
fun main(){
    HelloWorld() //HelloWorld 출력
}

fun HelloWorld(){
    println("HelloWorld")
}
```
return 값이 없는 함수일 경우 return type을 생략 가능
