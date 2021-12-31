# guard let ?
```guard``` 뒤에 따라붙는 코드의 실행 결과가 true 일 때 코드가 계속 실행된다.
- guard let 과 if let 둘 다 Optional 일때만 사용 가능하다.
- if 구문과는 다르게 ```guard``` 구문은항상 ```else``` 구문이 뒤에 따라와야 한다.

만약 ```guard``` 뒤에 따라오는 ```Bool``` 값이 false 라면 else 의 블록 내부 코드를 실행한다.   
- 이 내부 코드에는 자신보다 상위 코드 블록을 종료하는 코드가 반드시 들어가게 된다.

```return, break, throw``` 등

Bool 타입의 값으로 guard 구문을 동작시킬 수 있지만 <b>옵셔널 바인딩</b> 역할도 할 수 있다. 이렇게 사용하면 <b>guard 로 옵셔널 바인딩 된 상수</b>를 guard 구문 실행 코드 아래부터 <b>함수 내부의 지역상수처럼 사용 가능하다.</b>

## 장점
guard 구문 사용시 if 코드를 훨씬 간결하고 읽기 좋게 구성 가능하다.
예외사항만을 처리하고 싶다면 guard 구문을 사용하는 것이 훨씬 간편하다.

아래의 코드처럼
```swift
func ullName(name : String, rawPrefix : String?) {
    guard let prefix = rawPrefix else {
        return 
    }
    print(prefix)
}
```


## if let 
if let 으로 옵셔널 바인딩 된 상수는 그 블럭 안에서만 변수가 사용 가능하다.

#### 옵셔널 바인딩이란?
아래 링크를 보자
- [Optional Binding](https://github.com/Mindohyeon/TIL/blob/main/Swift/Swift/Optional%20Binding.md)