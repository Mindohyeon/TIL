# DAO (Data Access Object)란?
- 실제로 DB 에 접근하는 객체이다.
- Service 와 DB 를 연결하는 고리 역할을 한다.
- SQL 을 사용하여 DB 에 접근한 후 적절한 CRUD API 를 제공한다.
  - JPA 대부분의 기본적인 CRUD 메서드를 제공하고 있다.

<b>CRUD 란?</b> : 대부분의 컴퓨터 소프트웨어가 가지는 기본적인 데이터 처리 기능인 Create(생성), Read(읽기), Update(갱신), Delete(삭제)를 묶어서 일컫는 말이다.

# DTO (Data Transfer Object)란?
- 계층간 데이터 교환을 위한 객체이다.
  - DB에서 데이터를 얻어 Service 나 Controller 등으로부터 보낼 때 사용하는 객체를 말한다.
  - 로직을 갖고 있지 않는 순수한 데이터 객체이며, getter/setter 메서드만을 갖는다.
  - 하지만 DB 에서 꺼낸 값을 임의로 변경할 필요가 없기 때문에 DTO 클래스에는 setter 가 없다. (대신 , 생성자에서 값을 할당한다.)
