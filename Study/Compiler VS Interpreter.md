# Compiler VS Interpreter

## Compiler
1. 프로그램 runtime(실행시간) <b>전에</b> 전체 코드를 검사하여 lower level language(ex: 어셈블리어 언어, machinecode) 로 변환한다.

2. 소스 코드를 <b>분석</b>하는데 <b>많은 시간</b>이 필요하다.
그러나, <b>전체 실행 시간은 Interpreter 보다 비교적 빠르다.</b>

3. linking 을 추가로 필요로 하는 중간 공간 Object Code(목적 코드) 를 생성하기 때문에 <b>많은 메모리</b>가 필요하다.

4. 전체 코드를 검사한 후에 오류 메세지를 생성한다. 즉, 실행 전에 오류를 발견할 수 있다.

### Compiler 를 사용하는 언어
C, C++, Java

## Interpreter
1. 프로그램 runtime 한 번에 한 문장씩 변환한다.

2. 소스코드를 <b>분석</b>하는 <b>시간이 적다.    
</b>하지만, <b>전체 실행 시간</b>은 Compiler 로 변환한 코드보다 상대적으로 <b>느리다.</b>

3. 중간에 Object Code 가 만들어지지 않기 때문에 메모리 효율이 높다.

4. 첫 오류를 만날 때까지 프로그램을 번역하고, 오류를 만나면 중지한다. 프로그램 실행 전에 오류를 발견하기는 어렵다. 

### Interpreter 를 사용하는 언어 
Python, Ruby