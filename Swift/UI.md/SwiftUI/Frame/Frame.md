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
