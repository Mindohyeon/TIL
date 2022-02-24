# Array
### 타입 추론으로 생성하기
```swift
var array1 = [1,2,3]
var array2 = [] //error!!
```
타입 추론으론 빈 배열을 생성할 수 없다.

### 타입 어노테이션으로 생성하기
```swift
var array3 : [Int] = [1,2,3]
var array4 : [Int] = []
```

### 생성자로 생성하기
생성과 동시에 초기화
```swift
var array5 = Array<Int>()
var array6 = [Int]()

//생성과 동시에 10개의 요소 생성 및 0으로 초기화
var array7 = [Int](repeating : 100, count : 0)
```
## init(repeating: count:)
repeating 에는 반복할 문자나 숫자 등을 넣어주고, count 에는 반복 숫자를 넣어주면 된다.

#### String에서 사용
```swift
let apple = Strig(repeating: "사과", count: 3)
// 사과사과사과
```

#### Array 에서 사용
```swift
let lie = Array(repeating: false, count 5)
//[false, false, false, false, false]
```