# Compiler VS Interpreter

## Compiler
1. 프로그램 runtime 전에 전체 코드를 검사하여 machine code 로 변환한다.

2. 소스 코드를 분석하는데 많은 시간이 필요하다.
그러나, <b>전체 실행 시간은 Interpreter 보다 비교적 빠르다.</b>

3. linking 을 추가로 필요로 하는 중간 공간 Object Code를 생성하기 때문에 <b>많은 메모리</b>가 필요하다.

4. 전체 코드를 검사한 후에 오류 메세지를 생성한다. 즉, 실행 전에 오류를 발견할 수 있다.

#### Compiler 를 사용하는 언어
C,C++,Java