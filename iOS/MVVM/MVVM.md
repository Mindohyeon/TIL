# MVVM(Model - View - ViewModel)

## 'M'VVM 의 Model
MVVM 아키텍쳐에서 Mdel은 <b>데이터 구조를 정의</b>하고 ```ViewModel``` 에게 <b>결과를 알려준다.</b>
여기서의 Model 은 View 와 이어지지 않는다.

## M'V'VM 의 View 
MVVM의 View 는 흔히 사용하는 ```ViewController``` 에 코드를 작성한다.
View 는 사용자와의 상호작용을 통해 이벤트가 일어나게 되면 <b>ViewModel 에게 알려주고, ViewModel이 업데이트 요청한 데이터를 보여준다.</b>