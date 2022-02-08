# 메모리를 참조하는 방법 (Strong, Weak, Unowned)

## Strong
- 해당 인스턴스의 소유권을 가진다.
- 자신이 참조하는 인스턴스의 retain count 를 증가시킨다.
- 값 지정 시점에 retain이 되고 참조가 종료되는 시점에 release 된다.
- 선언할 때 아무것도 적어주지 않으면 default 로 Strong 이다.