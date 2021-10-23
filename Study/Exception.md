# Exception(예외)

## Checked Exception

### 특징
<b>반드시 예외 처리를 해야한다.</b>   
확인 : 컴파일 단계   
예외 발생신 트랜잭션 처리 : <b>roll-back 진행하지 않음</b>

### 대표적 예외
<b>RuntimeException</b> 을 제외한 거의 모든 예외


## Unchecked 

### 특징
<b>예외 처리를 반드시 하지 않아도 된다.</b>(필수 x)   
확인 : 컴파일 단계   
예외 발생신 트랜잭션 처리 : <b>roll-back 진행</b>

### 대표적 예외
RuntimeException 하위 예외
- NullPointerException    
- IllegalArgumentException
- IndexOutOfBoundException
- SystemException

## NPE 란?
<b>NullPointerException</b> : null 때문에 발생하는 Runtime Exception

### 가장 큰 문제
- null 자체의 의미가 모호해 다양한 파생 에러 발생한다.
- 에러 발생 이후 디버깅이 어렵다.

### 예방법
- null Parameter 를 넘기지 말자
- null 여부 비교 처리 추가
- 문자열을 비교시 equals 문자열을 먼저 위치 하자. (또는 Constants 사용)