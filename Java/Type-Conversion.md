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
