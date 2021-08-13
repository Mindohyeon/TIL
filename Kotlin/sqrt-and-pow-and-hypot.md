# sqrt
수의 제곱근을 구할 수 있다.

# pow
수(n)의 제곱을 구할 수 있다.

# hypot
두 수 각각의 제곱 수를 합한 수의 제곱근을 구할 수 있다.

---
```kotlin
fun main(args : Array<String>){
    var x : Double = 12.0
    var y : Dobue = 5.0


    println("===============제곱근==================")
    // println(Math.sqrt(x))   // java.lang.sqrt
    println("${x}의 제곱근 = ${sqrt(x)}") //4.0
    println("${y}의 제곱근 = ${sqrt(y)}") //2.236 ...


    println("===============제곱==================")
    println("${x}의 제곱 = ${x.pow(2)}") //256.0
    println("${y}의 세제곱 = ${y.pow(3)}") //125.0
}
```