# Range

## Closed Range
가장 기본 타입이며, 시작 값과 끝 값이 명확한 값의 범위를 나타내는 타입이다.

```swift
1...10 //1부터 10까지
1..<10//1부터 9까지
```

```swift
(1...10).lowrBound //1 
(1...10).upperBound //10
(1...10).count //10
```
Range 는 말 그대로 범위를 다룰 뿐 해당 범위 내의 여러 아이템의 실체는 존재하지 않는다.

## Partical Range
시작이나 끝이 생략된 형태의 범위를 말한다.

```swift
10... // 10이상
...10 // 10이하
..<10 //10 미만

```
보다시피 Closed Range 의 한 쪽이 사라진 형태이다.   


또한 containers() 와 같은 메서드를 제공한다.

이렇게 쓸 수도 있고
```swift
(10...).containers(20) // true
(10...).containers(3) // false
```

그러나 이런 경우에는 논리식으로 쓸 수 있다.

```swift
10 =< 20 // true
10 =< 3 // false
```