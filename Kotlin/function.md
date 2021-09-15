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

## filter
- filter 함수는 Array , List , Set, Map 에서 사용할 수 있다.
- 특정 조건을 주면 조건에 해당하는 원소를 찾아준다.
- for문과 if문으로도 결과를 얻을 수 있지만, filter 함수를 사용하면 간단하게 구현 가능하다.


## 고차 함수
함수를 클래스에서 만들어 낸
```instance```처럼 취급하는 방법

- 함수를 ```parameter```로 넘겨줄 수 있다.
- 함수를 결과값으로 반환 받을 수 있다.


