# 조건문
- return 값이 없을 경우 type생략이 가능하다

```kotlin
fun main(){
    println(maxBy(3 , 5)) // 5 출력
}

fun maxBy(a : Int , b : Int) : Int{
    if(a > b){
        return a
    }
    else {
        return b
    }
}
```

위의 예시는 아래와 같다

```kotlin
fun maxBy2(a : Int , b : Int) : Int = if(a>b) a else b
```
