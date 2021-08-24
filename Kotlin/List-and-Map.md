# List / Map

## List

#### List : Immutable
```listOf<타입>(아이템)```으로, Immutable List를 생성 및 초기화 할 수 있다. 코틀린은 아이템 타입을 스스로 추론하기 때문에 타입은 생략 가능하다.
- Immutable(불변의) 이기 때문에 get만 가능하다.

#### List : Mutable
수정 가능한 List는 mutableListOf로 선언한다. listOf와 차이점은 추가 및 삭제가 가능하다. 즉, 읽기/쓰기 모두 가능하다. (add, remove 등)