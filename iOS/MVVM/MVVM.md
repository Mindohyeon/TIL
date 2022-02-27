# MVVM(Model - View - ViewModel)

## Model
데이터 모델, 데이터 접근 레이어, 비즈니스 로직이 포함되어 있다.

MVVM 아키텍쳐에서 Mdel은 <b>데이터 구조를 정의</b>하고, <b>데이터의 흐름에 관하여 알고있다.</b> 이 작업들은  ```ViewModel``` 에 의해 작동되고, ```Model```이 데이터에 대한 작업을 마치면 ```ViewModel```에게 <b>결과를 알려준다.</b>

## View 
데이터를 표시하는 UI를 담당한다.
MVVM의 View 는 흔히 사용하는 ```ViewController``` 에 코드를 작성한다.
View 는 사용자와의 상호작용을 통해 이벤트가 일어나게 되면 <b>ViewModel 에게 알려주고, ViewModel 에서 처리한다. ViewModel의 변경사항을 감지하고, ViewModel이 업데이트한 데이터를 보여준다.</b>
> <b>여기서의 Model 은 View 와 이어지지 않는다. 오직 ViewModel 에 의해서 연결된다.</b>

## ViewModel
주요 로직을 담당한다. <b>이벤트를 처리할 때 Model 을 업데이트 하고 그 결과를 다시 받아와서 View 에게 전달하여 UI 를 업데이트 해야하는 책임을 가지고 있다.</b>
ViewModel 은 사용자의 상호작용을 view 가 보내주면 그에 맞는 이벤트 처리를 하고,
 Model의 Read, Update,  Delete 를 담당한다.
<b>객체를 쉽게 관리할 수 있다.</b> ViewModel 은 화면 표현의 대부분을 처리한다. 

<img src="../../Image/MVVM-img.png">

기존의 view 는 단순히 유저 인터페이스를 표시하기 위한 로직을 담당하고, 그 외에는 메소드 호출 정도만 있는게 이상적인데, 
```ViewModel``` 은 <b>기존 UIKit을 import 할 필요도 없이 데이터 업데이트 및 뷰 요소를 업데이트 한다.</b>

## MVVM 의 장단점

### 장점
- View - Model - ViewModel 모두 독립적으로 테스트가 가능하다.

### 단점 
- 설계가 어렵고, 뷰에 대한 처리가 복잡해지면 ViewModel 도 거대해진다.

## 정리
<b>ViewMoel 에서는 주오 로직을 담당해서 ViewController 에 전달해주면 ViewController 에서는 오직 UI 만 바꿔준다.</b> 이것이 MVVM 의 원리이다.
<b>ViewModel 은 view에 관한 어떠한 의존성이나 연결성도 없다.</b> 이것들이 다른 패턴들과의 차이인 것 같다.

##### 뷰와 관련된 데이터 상태를 ViewModel 이 가지고 있고, ViewModel 이 변경 되면 연결된 ViewController 나 View 가 바뀌도록 처리한다.


 #### 참고
 - https://42kchoi.tistory.com/292
 - https://velog.io/@gomminjae/Swift-MVVM