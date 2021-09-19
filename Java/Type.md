# Type

## Object Type
자바의 모든 객체들은 <b>```Object``` 란 클래스를 상속받는다.</b>

임의의 ```Class``` 를 만든다고 해도 그 클래스는 ```Object Class``` 를 ```default``` 로 상속받고 있다.

```public class AClass{}``` 는 사실상 ```public class AClass extends Object {}``` 가 된다.

그래서 객체를 만들면 Object 를 상속받지 않았더라도 equals 메서드나 toString 메서드를 사용한다.   
대부분 재정의 해서 사용한다.

<b>자바의 모든 객체를 관리하기 위해 Object 라는 Class 를 만들어 둔다.</b>







