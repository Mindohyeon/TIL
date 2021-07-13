# 배열
- 코틀린에서 배열은 Array 클래스로 표현된다.  
  해당 클래스는 get과 set함수 등을 가지고 있다.


```kotlin
fun main(args: Array<String>){
    var a = arrayOf(1,2,3)

    println(a.get(0))   // 1
    println(a.get(1))   // 2
    println(a.get(2))   // 3

    println(a[0])       // 1
    println(a[1])       // 2
    println(a[2])       // 3

    a[0] = 100          //a의 0번째 배열을 100으로 초기화
    a.set(1,200)        //a의 1번째 배열을 200으로 초기화

    println(a[0])       // 100
    println(a[1])       // 200
    println(a[2])       // 3
}
