# 고차함수(Higher-order-function) ?
다른 함수를 전달인자로 받거나 함수 실행의 결과를 함수로 반환하는 함수를 뜻한다.

Swift 의 함수는 일급시민이기 때문에 함수의 전달인자로 전달할 수 있으며, 함수의 결과값으로 반환할 수 있다.

- Map
- Filter
- Reduce

## Map
제공된 클로저를 각 항목에 적용한 후, 원래의 순서와 같도록 배치한 뒤 반환하는 메소드이다. 기존의 데이터를 변형하여 새로운 컨테이너를 생성하는 것이다.   

for 구문과 비슷하게 사용할 수 있지만, map 을 사용하게 되면 클로저 상수를 통해 <b>코드의 재사용이 용이</b>해지고 <b>컴파일러 최적화 측면에서 성능이 좋아진다.</b>

### 선언
```
배열.map( { (변수명 : 타입) -> 리턴타입 in 내용})
```

비교해보자.

먼저 for 구문이다.
```swift 
let number : [Int] = [0,1,2,3,4]
var doubleNumber = [Int] ()

for(num in number) {
    doubleNumber.append(num * 2)
}
//[0,2,4,6,8]
```
아래는 map 메서드를 사용한 예제다.
```swift
let number : [Int] = [0,1,2,3,4]
var doubleNumber = [Int]()

doubleNumbe = number.map( { (num : Int) -> Int in
    return num * 2
})
//[0,2,4,6,8]
```

map 메서드를 통해 값을 하나씩 받아와 클로저를 통해 값을 반환해준다.

## Filter
반환타입이 Bool 인 매개변수 함수의 결과가 true 면 새로운 컨테이너에 값을 담아 반환한다.
```swift
let arr = [0,1,2,3,4]
let filterArray = arr.filter { $0 % 2 == 0 }
print(filterArray) // [0,2,4]

```

## Reduce
데이터를 합쳐주기 위해 사용한다.
기존 컨테이너에서 내부의 값들을 결합하여 새로운 값을 만든다.  

- () 안에 초기값을 설정한다.

```swift
let arr = [0,1,2,3,4]
let reduceArray = arr.reduce(0) {$0 + $1}
print(reduceArray) //10
```