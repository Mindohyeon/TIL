# Error

### The local variable '변수명' may not have been initialized
```java
public static void main(String[] args) {
    String a;
    a = a + "B";   //error

}
```
<b>변수를 선언하기만 하고 값을 넣어주지 않아서 뭔가를 할 수 없는 상태</b>인데 거기에 + 를 하려고 했기 때문에 에러 발생