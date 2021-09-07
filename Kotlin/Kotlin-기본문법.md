# Kotlin 기본 문법

## 변수  
+ 자료형(type)을 명시해주지 않아도 자료형 추론이 가능
> 선언 방법  
+ var/val 변수명 : 자료형 = 값

>### 1. var = variable   
 - 읽기/쓰기가 모두 가능한 변수  
 -> 할당 후 변경이 가능하다.
 ```kotlin
 var a : Int = 10
 a = 30
 ```
>### 2. val = valuable  
 + 읽기만 가능한 변수  
 ->할당 후 변경이 불가능하다
```kotlin
val b : Int = 10
b = 30  //오류 발생
```

## null  
- 코틀린의 기본 변수는 null을 가질 수 없다. 따라서 늦은 초기화를 하려면 null 값을 초기에 명시해야한다.
- 변수에 null 값을 넣으려면 타입명 뒤에 ?를 붙이고 null값을 넣어야 한다.
```kotlin
var temp: String = "ABCD"
temp = null // 문법 오류
```
- return type 에 ? 가 붙으면, return type 이 null 이 될 수 있다는 의미이다.
```kotlin
var temp: String? = "ABCD"
temp = null
```

--- 
## 함수
> Kotlin의 함수 선언 방법
+ fun 함수명(변수명 : 변수 타입) : 리턴타입  

+ Java에서의 void 는 kotlin에서 Unit 이다.  

### 1.
> return값이 없는 함수일 경우 return type을 생략 가능
```kotlin
fun main(){
    HelloWorld() //HelloWorld 출력
}

fun HelloWorld(){
    println("HelloWorld")
}
```
### 2.
>  return값이 있는 함수일 경우 return type 필요
```kotlin
fun main(){
    println(add(4, 5))  //9출력
}

fun add(a : Int, b : Int) : Int{
    return a + b
}
```  
---

## 조건문(if)

+ if문도 return값이 없을 경우 type생략이 가능하다.  
  
 ### 1. 

```kotlin
fun main(){
    println(maxBy(3, 5)) // 5 출력
}

fun maxBy(a : Int , b : Int) : Int{
    if(a>b){
        return a
    }
    else {
        return b
    }
}
```
### 2. 
```kotlin
fun maxBy2(a : Int , b : Int) : Int = if(a>b) a else b
```
---
## when
+ return 값이 있을 경우에 else를 꼭 써야 함
>선언 방법  
+ when(변수명){  
 입력 받을 인수 -> 입력 받았을 때 출력  
}
+ 입력 받을 인수는 한 번에 여러 개 입력 가능  
ex) 1,2 -> println("1 or 2")


### 1.
> return 값이 없기 때문에 else  생략 가능
```kotlin

fun main(){
    checkNum(3)   // this is 2 or 3 출력
}

fun checkNum(score : Int) {
    when (score) {  =
        0 -> println("this is 0")
        1 -> println("this is 1")
        2, 3 -> println("this is 2 or 3")
        else -> println("I don't know")// 생략 가능
    }
}
```

### 2.
>return 값이 있기 때문에 else 생략 불가능
```kotlin
fun main(){
    checkNum(3) 
}
fun checkNum(score : Int) {
 var b = when (score) {   
        1 -> 1
        2 -> 2
        else -> 3
    }
    println("b : ${b}")  // b : 3 출력
}
```
---
## range
> + 주로 if문이나 for문에서 사용된다.    
> + 범위를 지정해준다.
> + for문은 c언어 등과 거의 비슷함
### 1.  ..  
+ 시작값부터 마지막값까지 증가한다.

> 선언방법
+ 변수명 in 시작값..마지막값
+ 
```kotlin
 var sum : Int = 0
    for(i in 1.. 10){ 
    sum +=i
    }
    println(sum) // 55출력
```

### 2.  step 
+ 일정 간격으로 수를 건너뛸 수 있다.
> 선언방법  
+ 변수명 in 시작값..마지막값 step 간격
 
```kotlin
 var sum : Int = 0
    for(i in 1.. 10 step 2){ 
    sum +=i
    }
    println(sum) // 25출력
```

### 3. downTo
+ 시작값부터 마지막값까지 감소한다
>선언방법
+ 변수명 in 시작값 downTo 마지막값 

```kotlin
var a : Int = 0
    for(i in 10 downTo 1){ 
        a +=i
    }
    println(a)
```
### 4. until  
+ 시작값부터 마지막값 미만까지 증가한다.
>선언방법
+ 변수명 in 시작값 until 마지막값

```kotlin
  var b : Int = 0
    for(i in 1  until 100){  
        b+=i
    }
    println(b)
```

## get / set

### get
자동 호출되어 값을 가져온다.

### set
자동 호출되어 값을 수정할 수 있다.


# List / Map

## List

#### List : Immutable
```listOf<타입>(아이템)```으로, Immutable List를 생성 및 초기화 할 수 있다. 코틀린은 아이템 타입을 스스로 추론하기 때문에 타입은 생략 가능하다.
- Immutable(불변의) 이기 때문에 get만 가능하다.

#### List : Mutable
수정 가능한 List는 mutableListOf로 선언한다. listOf와 차이점은 추가 및 삭제가 가능하다. (add, remove 등)
























 
 
 