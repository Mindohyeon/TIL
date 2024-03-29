# TCP Connection (3-Way Handshake) 란?
TCP는 장치들 사이에 논리적인 접속을 성립하기 위하여 Three-Way Handshake 를 사용한다.

- 연결 요청을 보낼 때 (SYN)

## 역할
- 양쪽 모두 데이터를 전송할 준비가 되었다는 것을 보장한다.
- 실제로 데이터 전달이 시작하기 전에 한쪽이 다른 한쪽이 준비되었다는 것을 알 수 있도록 한다.
- 양쪽 모두 상대편에 대한 초기 순차일련번호를 얻을 수 있도록 한다.

#### UDP 의 단점을 극복했다

<img src="Image/../../Image/225A964D52F1BB6917.png">    

SYN : synchronize sequence numbers = 연결요청
ACK : acknowledgment = 응답
FIN : Finish = 연결종료 요청

A -> B : 살아있어?   
B -> A : 응, 너는?   
A -> B : 나도! 

마지막으로 ```Client```가 ```Server```에게 ```ACK``` 를 보낸 이후부터는
서로 연결이 이루어지고 데이터가 오갈 수 있다.
# 4-Way HandShake

- 연결 종료 요청을 보낼 때 (FIN)

<img src="Image/../../Image/99CDF7445B5950990D.png">

--- 
# Question
#### TCP의 연결 설정 과정과 연결 종료 과정 단계가 차이나는 이유?
- Client가 전송을 마쳤다 하더라고 Server는 아직 보낼 데이터가 남아있을 수 있음. 
때문에 FIN 에 대한 ACK 만 보내고, 데이터를 모두 전송한 후 자신도 FIN 을 보내기 때문이다.

