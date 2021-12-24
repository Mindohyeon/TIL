# viewWillApear 란?
뷰가 나타날 때 마다 로직이 실행된다.

하지만 , 앱이 처음 실행될 때를 제외하고는 뷰가 화면에 나타나도 다시 ```viewWillAppear``` 가 호출되지 않는다.

#### 이유
 애플이 iOS 13부터 기본 프레젠테이션 스타일을 풀 스크린이 아닌 형태로 변경했기 때문에, 현재 뷰 컨트롤러를 닫더라도 ```viewWillAppear``` 를 호출하지 않기 때문이다.

 ### 해결
 Segue 를 통해 화면을 이동할 때, 기본 ``Presentation`` 스크린을 ```Full Screen```으로 변경해주면 viewWillAppear 가 매번 실행된다.