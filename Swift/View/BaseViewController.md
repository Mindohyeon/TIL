# BaseViewController 란?
기본적으로 ViewController 를 만들면 UIViewController 를 상속받게 된다.

여기서 받은 UIViewController 에 사용하기 편하게 추가로 BaseViewController 라는 걸 만들어 줘서 <b>UIViewController 대신 BaseViewController 를 상속시켜주면 된다.</b>

- 어차피 BaseViewController 가 UIViewController 를 상속받기 때문에 괜찮다.

## BaseViewController 사용 이유
중복적으로 사용되는 코드를 중복 없이 만들 수 있다.

예를 들자면 ,
- 뷰의 배경화면이 거의 흰색인 경우
- 반복적으로 라이브러리를 사용할 때 뷰컨트롤러 마다 import 를 해줘야 하는 경우
- 항상 사용하는 변수가 있는 경우

이럴 때, 뷰컨트롤러 마다 중복적으로 적어줘야 하는 부분들이 있다.
이러한 부분을 BaseViewCon 를 따로 정의하고, BaseViewController 를 상속 받아 주면 중복 없이 코딩할 수 있게 된다.

#### 정리
<b>통일성 있고, 가독성 있게 코딩할 수 있다.</b>