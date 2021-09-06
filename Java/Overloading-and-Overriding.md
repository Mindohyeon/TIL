# Overloading 이란? (오버로딩)
- 같은 이름의 메서드를 여러개 가지면서 매개변수의 유형과 개수가 다르도록 하는 기술

```kotlin
class OverloadingTest{
    //이름이 otl인 메서드
    void otl(){
        System.out.println("매개변수 없음");
    }
    
    //매개변수 int형이 2개인 otl 메서드
    void otl(int a, int b){
        System.out.println("매개변수 :" + a + ", " + b);
    }
    
    //매개변수 String형이 한 개인 otl 메서드
    void otl(String c){
        System.out.println("매개변수 : " + c);
    }
}

public class test {
 
    public static void main(String[] args) {
        
        //OverloadingTest 객체 생성
        OverloadingTest ot = new OverloadingTest();
        
        //매개변수가 없는 otl() 호출
        ot.otl();
        
        //매개변수가 int형 두개인 otl() 호출
        ot.otl(20, 70);
     
        //매개변수가 String 한개인 otl() 호출
        ot.otl("오버로딩 예제");
    }
}
```

### output
```kotlin 
매개변수 없음
매개변수 :20, 70
매개변수 : 오버로딩 예제
```

# Overriding 이란? (오버라이딩)
- 상위 클래스가 가지고 있는 메서드를 하위 클래스가 재정의해서 사용