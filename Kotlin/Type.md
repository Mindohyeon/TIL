# Type

Java Type | Kotlin Type | Kotlin Type 용량(bit)
--- | --- | --- 
double | Double | 64
float | Float | 32
long | Long | 64
int | Int |32
short | Short | 16
byte | Byte | 8




## Byte
#### range : -128 ~ 127

일반적으로 memory 사용을 줄이기 위해 [-128, 127] 사이의 integer data를 표현하기 위한 목적으로 <b>Int type 대신 사용된다.</b>


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

toLong(): Long

toFloat(): Float

toDouble(): Double

toChar(): Char




