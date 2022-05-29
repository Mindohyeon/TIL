# Function

## 가변 매개변수 (...)
함수에 전달될 인수의 수를 미리 알지 못할 때 사용한다.

```...``` 은 가변 매개변수를 나타내기 위해 매개변수 유형 뒤에 사용한다.

```swift
func addSubviews(_ subView: UIView...) {
    subView.forEach(addSubview(_:))
}
```



#### 참고
- https://www.programiz.com/swift-programming/function-parameter-return-values