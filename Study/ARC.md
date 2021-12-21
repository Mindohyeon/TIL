# ARC(Auto Reference Counting)란 ? 
- <b>자동</b>으로 <b>메모리를 관리</b>해준다.
- 객체에 대한 <b>참조 카운트</b>를 관리하고 <b>0</b> 이 되면 자동으로 <b>메모리를 해제한다.</b>
- <b>run time</b>에 계속 실행되는 게 아니라 <b>compile time(build 할 때)</b> 에 실행
- <b>Retain cycle</b> 에 유의해야 한다.

> ARC <-> MRC