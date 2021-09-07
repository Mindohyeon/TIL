# Access Modifier 이란 ? (접근 제어자)
선언한 해당 항목의 범위를 제한하는 것이 목적이다.

### 사용
클래스 , 변수 , 메서드 등을 선언할 때 사용한다.

## 접근 범위
|  |해당 클래스 안에서|같은 패키지에서|상속 받은 클래스에서|import한 클래스에서|
|--|---------------|---------------|--------------------|--------------------|
|public| <center>O|<center>O|<center>O|<center>O|
|protected|<center>O|<center>O|<center>O|<center>O|
|(package private)|<center>O|<center>O|<center>X|<center>X|
|private|<center>O|<center>X|<center>X|<center>X|