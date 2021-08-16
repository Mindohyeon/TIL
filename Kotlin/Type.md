# Type

Java Type | Kotlin Type | Kotlin Type 용량(bit)
--- | --- | --- 
byte | Byte | 8
short | Short | 16
int | Int |32
long | Long | 64
double | Double | 64
float | Float | 32


## Byte

#### range : -128 ~ 127

일반적으로 memory 사용을 줄이기 위해 [-128, 127] 사이의 integer data를 표현하기 위한 목적으로 <b>Int type 대신 사용된다.</b>

## Short

#### range : -32768 ~ 32767

memory 사용을 줄이기 위해 [-32768, 32767] 사이의 integer data를 표현하기 위한 목적으로 <b>Int type 대신 사용된다.</b>

## Int

#### range : -2147483648 ~ 2147483647

type을 명시적으로 작성하지 않으면 Int type 으로 자동 설정된다.

## Long

#### range : -9223372036854775808 ~ 9223372036854775807

명시적으로 Long type 변수를 사용하려면 <b>'L'</b>을 숫자에 함께 붙여주면 된다.
```kotlin
val value = 100L //Long type 이라는 의미
```
## Double 

#### Double type : double-precision 64 bit floating point

double-precision 은 8 byte(64 bit) 로 표현되고 ,   
이 64 bit 는 <b>sign , exponent , fraction bit</b> 로 구성된다.

- sign(S) : 0 번째 bit   
- exponent(E) : 1 ~ 11 번째 bit   
- fraction(F) : 나머지 bit

```kotlin
fun main(args: Array<string>){
    val value = 1032.1
    println("$value")
}
```

## Float

#### Float type : single-precision 32 bit floating point

single-precision 은 4 byte(32 bit) 로 표현되고 ,   
 이 32 bit는 <b>sign , exponent , fraction bit</b> 로 구성된다.   
이를 표현하기 위해서는 literal constant 에 <b>F</b>를 붙여야 한다.

---
## literal 이란?

<b>변수의 값이 변하지 않는 데이터</b> (메모리 위치 안의 값)을 의미한다.


#### constant (상수) 란?

<b>변하지 않는 변수</b>를 의미하고(메모리 위치) 메모리 값을 변경할 수 없다.

---

- sign(S) : 0번째 bit (부호)
- exponent(E) : 1 ~ 8 번째 bit (지수)  
- fraction (F) : 나머지 bit

<b>F</b> 가 없는 Double type 의 literal 은 Float type 에 할당 할 수 없다.
```kotlin
fun main(args: Array<string>){
    val value = 1032.1F
    value = 1024.2
    println("$value") //오류 발생
}
```
---
## 명시적 type 변환

```kotlin
val a: Int? = 10 
val b: Long? = a //오류 발생
var b : Long? = a.toLong() 
print(b == a)
```
오류가 발생한 이유는 Int형 10을 Long형의 변수에 할당하려고 했기 때문이다. 
<b>즉 , Int 10 과 Long 10 은 다르다.</b>

### 모든 number type 은 다음과 같은 function 을 통해 변환이 가능하다.

#### toByte()
다른 number type 의 변수를 Byte 형태로 바꿔준다.

#### toShort()
다른 number type 의 변수를 Short 형태로 바꿔준다.

#### toInt()
다른 number type 의 변수를 Int 형태로 바꿔준다.

#### toLong()
다른 number type 의 변수를 Long 형태로 바꿔준다.

#### toFloat()
다른 number type 의 변수를 Float 형태로 바꿔준다.

#### toDouble()
 다른 number type 의 변수를 Double 형태로 바꿔준다.

#### toChar()
다른 number type 의 변수를 Char 형태로 바꿔준다.




