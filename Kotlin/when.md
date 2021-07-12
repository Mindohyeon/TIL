# When 
- return 값이 있을 경우에 else를 꼭 써야 한다.

### 선언방법
- when(변수명){  
 입력 받을 인수 -> 입력 받았을 때 출력  
}

- 입력 받을 인수는 한 번에 여러 개 입력 가능  
ex) 1,2 -> println("1 or 2")

### return 값이 있는 경우
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
return 값이 있기 때문에 else 필수

### return 값이 없는 경우
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
return 값이 없기 때문에 else 생략 가능