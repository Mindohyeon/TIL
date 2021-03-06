# Combine
간단히 말하면 시간의 흐름에 따라 발생하는 이벤트를 처리하기 위한 Declarative Swift API 를 제공하는 프레임워크이다.

Combine 은 발생한 이벤트에 대해 어떻게 가공하고 소비해줄지에 초점을 맞춘다.
 비동기와 관련된 코드를 작성할 때 <b>사용하던 불필요한 보일러 플레이트를 줄여주며, 런타임 오류를 효율적으로 처리할 수 있고, 데이터의 제공자가 아닌 데이터 요청자 측에서 처리할 수 있다.</b>

<b>*보일러 플레이트 : 최소한의 변경으로 여러 곳에서 재사용되며, 반복적으로 비슷한 형태를 띄는 코드를 말한다.</b>


## Combine 을 이루는 3가지
<img src="../../../Image/SwiftUI-Combine-3가지.png">

Combine 은 크게 <b>Publisher, Operator, Subscriber</b> 로 이루어져 있다.
```Subscriber``` 로부터 데이터를 요청받으면 ```Publisher```에서 데이터를 제공하고 중간에 ```Operator``` 를 거쳐 ```Subscriber``` 에게 전달된다.

<img src="../../../Image/Publisher와Subscriber관계.png">

Publisher 와 Subscriber 가 서로 데이터를 주고받을 때 항상 두 가지의 타입이 존재한다.

publisher 입장에서는 에러가 발생했을 경우 Failure 타입 그렇지 않으면 Output 타입을 전달한다. 

##### 참고
- https://medium.com/harrythegreat/swift-combine-%EC%9E%85%EB%AC%B8%ED%95%98%EA%B8%B0-%EA%B0%80%EC%9D%B4%EB%93%9C-1-525ccb94af57
- https://www.hohyeonmoon.com/blog/combine-introduction/