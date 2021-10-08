# Constructor (생성자)
new 연산자와 함께사용되어 클래스로부터 객체를 생성할 때 호출되어 객체의 초기화를 담당한다.   
<b>주로 인스턴스 변수의 초기화 작업에 쓰인다.</b>

- 생성자의 이름은 클래스 이름과 동일해야 한다.
- 생성자는 리턴값이 없다.
- 생성자는 오버로딩이 가능하기 때문에 하나의 클래스에 여러 개의 생성자가 있을 수 있다. 
- 생성자도 메서드이기 때문에 리턴값이 없다는 의미로 void 를 적어야 하지만, 모든 생성자가 리턴값이 없으므로 void 를 생략하도록 한다.

```java
public class Ex08 {
	public static void main(String[] args) {
		
		Food chicken = new Food("치킨", 18000);
		Food pizza = new Food("피자", 28000);
		Food sushi = new Food("초밥세트",22000);
		
		//객체 배열에 음식 담기
		Food[] foods = {chicken, pizza, sushi };
		
		//모든 음식 정보 출력
		for(int i = 0;i < foods.length;i++) {
			foods[i].print();
		}			
	}
}
class Food {
	
	String name;
	int price;

    //생성자 생성
	Food(String name, int price) {
		this.name = name;
		this.price = price;
	}
	
	public void print() {
		System.out.printf("name : %s, price : %d\n",name,price);
	}
}
```

### 기본 생성자
모든 클래스는 생성자가 반드시 존재한다.   
만약 클래스에 정의된 생성자가 없으면 컴파일러가 자동적으로 생성자를 생성시킨다.