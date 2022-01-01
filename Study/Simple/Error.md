# 오류와 에러의 차이?

사실 오류와 에러 이 둘을 나눌수는 없다. 질문 자체가 틀린 것이다.

일단, 프로그램이 실행 중에 어떠한 원인에 의해 오작동을 하거나 비정상적으로 종료되는 경우를 프로그램 <b>오류</b> 라고 한다.

그리고 이러한 <b>오류</b> 안에 <b>에러(Error)</b> 와 <b>예외(Exception)</b> 두 가지로 구분할 수 있다.

둘은 큰 차이가 있다.

## Error
컴파일 시 문법적인 오류와 런타임 시 널 포인트 참조와 같은 오류로 프로세스에 심각한 문제를 야기시켜 프로세스를 종료 시킬 수 있다.

## Exception
컴퓨터 시스템의 동작 중에 예기치 않았던 이상 상태가 발생하여 수행 중인 프로그램이 영향을 받는 것이다.


## Error VS Exception
<b>Error</b> 는 메모리 부족이나 스택오버플로우와 같이 발생하면 복구할 수 없는 심각한 오류이고, <b>Exception</b>  은 발생하더라도 수습할 수 있는 비교적 덜 심각한 오류다.

Error 의 상황을 미연에 방지하기 위해 Exception 상황을 만들 수 있다. java 에서는 try-catch 문으로 Exception handling(예외처리) 을 할 수 있다.