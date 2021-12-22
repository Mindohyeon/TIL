# ARC(Auto Reference Counting)란 ? 
- <b>자동</b>으로 <b>메모리를 관리</b>해준다.
- <b>run time</b>에 계속 실행되는 게 아니라 <b>compile time(build 할 때)</b> 에 실행
- <b>Retain cycle</b> 에 유의해야 한다.
- 컴파일 시 코드를 분석해 retain , release 코드를 생성해 준다.
- 참조된 횟수를 추적해 더 이상 참조되지 않는 인스턴스를 메모리에서 해제해 준다.
- swift 는 ARC 를 사용하고 object - c 는 MRC 를 사용한다.

> ARC <-> MRC