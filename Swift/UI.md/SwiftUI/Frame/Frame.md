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

### padding
padding 을 줘서 직접 뷰간에 간격을 줄 수 있다.

```swift
Text("Hello").font(.title).padding()
```

padding 에 값을 주어 그 크기만큼 간격을 줄 수도 있다.

```swift
Text("Hello").font(.title).padding(10)
```

방향을 주어서 그 방향에만 간격을 줄 수도 있다.

```swift
Text("Hello").font(.title).padding(.top, 10)
```