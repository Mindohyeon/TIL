# 함수

- Java 에서의 void는 Kotlin 에서 Unit이다.

## 함수 형식 자료형으로 표현
()안에 함수가 받을 ```parameter```의 자료형 작성 후
-> 반환형쓰기

```kotlin
// 함수가 받을 parameter 자료형은 String 이고 반환형은 없다
fun b(function: (String) -> Unit) {

}
```


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

kotlin 의 모든 함수는 고차함수로 사용 가능.

- 함수를 ```parameter```로 넘겨줄 수 있다.
- 함수를 결과값으로 반환 받을 수 있다.

```kotlin
fun main() {
    
}

fun a(str: String) {
    println("$str 함수 a")
}

fun b(function: (String) -> Unit) {
    function("b가 호출한")
}
```
## 람다 함수
주로 고차 함수에 ```argument``` 로 전달되거나 고차 함수가 돌려주는 값으로 쓰인다.

### 사용 이유
- 코드의 간결함
- 지연 연산을 통한 퍼포먼스 향상
- iteration 코드를 구현하는 데 불필요한 부분들을 제거 가능


## 스코프 함수
```instance```의 속성이나 함수를 scope 내에서 깔끔하게 분리하여 사용할 수 있다.

### 종류
- apply
- run
- with
- also
- let


#### apply
```instance``` 생성 후 변수에 담기 전에 초기화 할 때 주로 사용한다.

```instance``` 자신을 다시 반환하기 때문에 생성되자마자 조작된 ```instance```를 변수에 바로 넣을 수 있다.
```kotlin
fun main() {
    var a = Book("코틀린", 10000).apply {
        name = "[초특가]" + name
        discount()
    }

class Book(var name: String, var price: Int) {
    fun discount() {
        price -=2000
    }
}
```
```instance```의 속성과 함수를 직접 참조 연산자 없이 가능하다