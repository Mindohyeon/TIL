# Frame

- Spacer
- aligment
- padding

### Spacer
배치된 뷰들의 간격을 제공하기 위해 스텍의 방향에 따라 확장, 축소 된다.

```swift
struct ContentView : View {
    
    var body : some View {

        VStack {
            Text("A")
            Spacer()    
            Text("B")

        }.frame(width: 100, height: 100, alignment: .center)
    }
}
```

이렇게 하면 세로로 공간이 생긴다.


### aligment 
aligment 는 정렬 방식을 말한다.

```swift
struct ContentView : View {
    
    var body : some View {

        VStack(aligment: .center, spacing: 10) {

            Text("First")
            Text("Second")
        }
    }
}
```
이렇게 하면 간격이 10이고 가운데 정렬이 된다.

.center = 가운데 정렬
.leading = 좌측 정렬
.trailing = 우측 정렬