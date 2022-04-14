# Functional Programming (함수형 프로그래밍)

- 상태값을 갖지 않고 순수하게 <b>함수만으로 동작이 동일한 input 에는 동일한 output 을 보장한다.</b>
- 상호 간섭 없이 실행되기 때문에 <b>병렬처리를 할 때 부작용이 거의 없다.</b>
- <b>함수를 일급 객체로 다룬다.
  - 함수를 객체로 다룰 수 있다.</b>

###### 일급 객체?
- [일급객체](https://github.com/Mindohyeon/TIL/blob/main/Study/Frist-Class-Object.md)


### 일급 객체 취급 함수?
```swift
func firstAction(){
  print("first action")
}

func secondAction(){
  print("second action")
}

//반환 타입이 Void 인 함수를 배열 매개변수로 가진다.
//만약 위 두 개의 함수 중 하나라도 반환 타입이 Void 가 아니라면 호출할 때 에러가 발생한다.
func allFunc(tasks: [() -> Void]){
  for task in tasks{
    task()
  }
}

allFunc(tasks: [firstAction, secondAction])
```

출력
```
first action
second action
```

함수가 일급객체로 취급되기 때문에 함수의 파라미터, 배열의 요소로 들어갈 수 있다.
