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

>### 3. null  
+ 코틀린의 기본 변수는 null을 가질 수 없다.
```kotlin
var temp: String = "ABCD"
temp = null // 문법 오류
```
+ return type 에 ? 가 붙으면, return type 이 null 이 될 수 있다는 의미이다.
```kotlin
var temp: String? = "ABCD"
temp = null
```




















 
 
 