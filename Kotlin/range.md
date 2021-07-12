# range
- 범위를 지정해주며 주로 If문이나 For문에서 사용된다.

## kind
- ..
- step
- downTo
- until

## ..
- 시작값부터 마지막값까지 증가한다.
### 선언방법
+ 변수명 in 시작값..마지막값
```kotlin
 var sum : Int = 0
    for(i in 1.. 10){ 
    sum +=i
    }
    println(sum) // 55출력
```

## step
- 일정 간격으로 수를 건너뛸 수 있다.

### 선언방법
- 변수명 in 시작값 .. 마지막값 step 간격
 
```kotlin
 var sum : Int = 0
    for(i in 1.. 10 step 2){ 
    sum +=i
    }
    println(sum) // 25출력
```

## downTo
- 시작값부터 마지막값까지 감소한다.
  
### 선언방법
- 변수명 in 시작값 downTo 마지막값
```kotlin
var a : Int = 0
    for(i in 10 downTo 1){ 
        a +=i
    }
    println(a)
```

## until
- 시작값부터 마지막값 미만까지 증가한다.

### 선언 방법
- 변수명 in 시작값 until 마지막값

```kotlin
var b : Int = 0
    for(i in 1 until 100){
        b+=i
    }
    println(b)
```
