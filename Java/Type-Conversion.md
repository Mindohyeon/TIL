# 형변환

```java
import java.util.Scanner;

public class PrimitiveTypes {
	public static void main(String[] args) {
		PrimitiveTypes types = new PrimitiveTypes();
		types.checkByte();
	}
	public void checkByte() {
		byte byteMin = -128;
		byte byteMax = 127;
		System.out.println("byteMin="+ byteMin);
		System.out.println("byteMax="+ byteMax);
		byteMin = (byte)(byteMin-1);
		byteMax = (byte)(byteMin+1);
		System.out.println("byteMin-1="+ byteMin);
		System.out.println("byteMax+1="+ byteMax);
	}
}
```
#### output

```java
byteMin=-128
byteMax=127
byteMin-1=127
byteMax+1=-128
```

최소값에서 1은 뺀 것은 최대값이, 최대값에서 1을 더한 것은 최소값이 나온 이유는   

byteMin 의 값, 즉 2진수로 표현하면 ```1000_0000```인 값에서 1을 빼면 ```0111_1111```이 된다.
