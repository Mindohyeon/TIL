# Collections
Collection 은 대부분의프로그래밍 언어에 있는 자료구조다.   
Java의 List,Map,Set 등을 말한다.

## List

#### List : Immutable
```listOf<타입>(아이템)```으로, Immutable List를 <b>생성 및 초기화 할 수 있다.</b> 코틀린은 아이템 타입을 스스로 추론하기 때문에 타입은 생략 가능하다.
- Immutable(불변의) 이기 때문에 get만 가능하다.

#### List : Mutable
수정 가능한 List는 mutableListOf로 선언한다. listOf와 차이점은 <b>추가 및 삭제가 가능하다. 즉, 읽기/쓰기 모두 가능하다. (add, remove 등)</b>

```kotlin
fun main() {
    val a = listOf("사과","딸기","배")
    //List a 의 1번째 index 값 출력
    println(a[1])

    //List a 에서 요소를 하나씩 fruit 변수에 할당
    for(fruit in a) {
        print("${fruit} :")
    }
    //줄을 바꾸기 위함
    println()

    val b = mutableListOf(6,3,1)
    println(b)

    //List 뒤에 4 추가
    b.add(4)
    println(b)

    //index 2번째에 8 추가
    b.add(2,8)
    println(b)

    //index 1번째 값을 삭제
    b.removeAt(1)
    println(b)

    //무작위로 섞기
    b.shuffle()
    println(b)

    // 오름차순으로 정렬
    b.sort()
    println(b)
}
```
### output
```kotlin
딸기
사과 : 딸기 : 배 :
[6 , 3 , 1]
[6 , 3 , 1 , 4]
[6 , 3 , 8 , 1 , 4]
[6 , 8 , 1 , 4]
[8 , 1 , 6 , 4]
[1 , 4 , 6 , 8]
```

## Set
순서가 정렬되지 않고, 중복이 허용되지 않는 컬렉션이다.

- index 로 위치를 지정하여 객체를 참조할 수 없다.
- contains로 객체가 Set 안에 존재하는지 확인하는 식으로만 사용한다.
```kotlin
//sampleSet 에 사과가 있는지 알려줌
sampleSet.contains("사과")
```



## MutableList 기능
- init
- add, addAll
- clear
- iterator, listlterator
- remove, removeAll
- removeAt
- retainAll
- set
- subList
- val,var

## add, addAll
```kotlin
fun main() {
    val mulist : MutableList<Int> = mutableListOf<Int>(10,20,12,36,55)

    mulist.add(100) //output: 10,20,12,36,55,100
    mulist.add(3,77)  //output: 10,20,12,77,36,55,100 (index 3번째 위치에 77 값을 넣는다.)

    val list = listOf<Int>(1,2,3)
    mulist.addAll(2,list)  //output: 10,20,1,2,3,12,77,36,55,100 (index 2번째 위치에 list에 값을 넣는다.)
}
```
<b>add</b> 를 실행하면 뒤에 붙여지거나 중간위치에 삽입이 가능하다.   
<b>addAll</b> 를 실행하면 collection 을 중간에 끼워넣을 수 있다.

## clear

```kotlin
fun main() {
    val mulist: MutableList<Int> = mutableListOf(10,20,16,77)
    mulist.clear()  //output: null
}
```
MutableList요소를 삭제 할 수 있다.

## remove, removeAll

```kotlin
fun main() {
    val mulist: MutableList<Int> = mutableListOf(10,20,16,77,55)

    mulist.remove(10)  //output: 20,16,77,55
    mulist.remove(100)  //output: 20,16,77,55

    val list: List<Int> = listOf<Int>(1,2,3,20)
    mulist.removeAll(list)  //output: 16,77,55
}
```
<b>remove</b>는 배열의 해당 요소값을 찾아 삭제하고, true 를 반환한다.
만약 해당 요소값이 없을 경우에는 값을 유지하며 false 를 반환한다.

## val, var
val 로 선언하든 var 로 선언하든 함수의 <b>추가, 삭제는 가능하다.</b>

하지만 <b>val</b>로 선언된 MutableList 는 새로운 MutableList 를 전달받을 수 없다.



