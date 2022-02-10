# Retain Cycle
- 메모리가 해제되기 않고 유지되어 누수가 생기는 현상을 말한다.

### 참조하는 값은 메모리의 어떤 부분에 해당될까?
바로 <b>Heap</b> 이라는 영역에 해당된다.

<b>Heap</b> 이라는 영역에 메모리가 저장되기 위해서는 한 공간이 필요한데, 바로 그 공간을 레퍼런스가 바라보고 있는 것이다.

<img src="../../Image/RetainCycle-Heap.png">

### Retain 이란?
먼저 <b>Retain</b> 이란 위 사진과 같이 메모리를 차지하고 있는 레퍼런스를 이용해서 인스턴스를 만들었을 때 생겨난다.

A를 클래스라고 가정하고 "let instance = A()" 라고 만들어 주는 것이 <b>retain</b> 되는 것이다.

<img src="../../Image/RetainCycle-Instance.png">

