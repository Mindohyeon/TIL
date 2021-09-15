# Object 란?
<b>생성자 없이</b> 객체를 만든다.
> ```instance``` 를 생성하지 않고 그 자체로 객체이다.

````Singleton Pattern```` 을 언어 차원에서 지원
> 하나의 객체로 공통적인 속성과 함수를 사용해야하는 코드에서 사용함

별도의 ```instance``` 를 생성하지 않기 때문에 ```Object``` 이름에 직접 참조연산자를 붙여 사용한다.

---
### Class 와 차이
인스턴스 객체를 만들기 위한 틀  

내부에 있는 속성이나 함수를 사용하려면 생성자를 통해 실체가 되는 ```instance``` 객체를 만들어야 한다.

---
```kotlin

fun main() {
    println(Counter.count)

    Counter.countUp()
    Counter.countUp()

    println(Counter.count)

    Counter.clear()

    println(Counter.count)
}

object Counter {
    var count = 0

    fun countUp() {
        count++
    }
    fun clear() {
        count = 0
    }
}
```
```Object``` 로 선언된 객체는 <b>최초 사용시 자동으로 생성</b>되며 코드 전체에서 <b>공용으로 사용될 수 있다. </b>  
때문에 프로그램 종료까지 공통으로 사용할 내용들을 묶어 만드는 것이 좋다.