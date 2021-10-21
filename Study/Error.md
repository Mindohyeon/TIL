# 각종 error

## NPE 란?
<b>NullPointerException</b> : null 때문에 발생하는 Runtime Exception

### 가장 큰 문제
- null 자체의 의미가 모호해 다양한 파생 에러 발생한다.
- 에러 발생 이후 디버깅이 어렵다.

### 예방법
- null Parameter 를 넘기지 말자
- null 여부 비교 처리 추가
- 문자열을 비교시 equals 문자열을 먼저 위치 하자. (또는 Constants 사용)