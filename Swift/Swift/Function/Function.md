# Function

## 가변 매개변수 (...)
함수에 전달될 인수의 수를 미리 알지 못할 때 사용한다.

```...``` 은 가변 매개변수를 나타내기 위해 매개변수 유형 뒤에 사용한다.

```swift
func addSubviews(_ subView: UIView...) {
    subView.forEach(addSubview(_:))
}
```

## 인수 레이블 생략
```_```을 매개변수 앞에 작성하여 인수 레이블을 생략할 수 있다.

```swift
func sum(_ a: Int, _ b: Int) {
  print("Sum:", a + b)
}
sum(2, 3)
```

- ```_```을 매개변수 이름 앞에 사용하면 인수 레이블이나 매개변수 이름 없이 함수를 호출할 수 있다.



#### 참고
- https://www.programiz.com/swift-programming/function-parameter-return-values