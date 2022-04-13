# Optional Chaining 이란?

옵셔널일 수 있는 인스턴스 내부의 프로퍼티, 메서드, 서브스크립트를 <b>매번 nil 체크 하지않고 최종적으로 원하는 값, 혹은 nil 인지 판단하는 방법이다.</b>

여러개를 함께 연결할 수 있고, 연결된 어떤 링크라도 nil 이면 nil 이 된다.

<b>하나의 링크라도 옵셔널이면 nil 값이 나온다.</b>

```swift

class Family {
    var child : Child?
}

class Child {
    var name : String?
}

var family = Family()
family.child?.name = "C"

let name = family.child?.name
print(name) //nil 출력
```

##### 이유는?

현재 Family 클래스 안에 있는 child 가 nil 이기 때문이다!!
```swift
class Family {
    var child : Child? 
}
class Child {
    var name : String?
}
```
이 부분에서 Child 클래스는 Optional 로 선언되어있기 때문에 애초에 Child 클래스는 nil 로 초기화 되어있는 것이다.

```swift
family.child?.name = "C"
```
따라서 이 방법으로는 ```child.name``` 을 초기화 할 수 없다.

##### 모든 링크에 인스턴스 참조
```swift
let family = Family()
let child = Child()

child.name = "dohyeon"

family.child = child
let name = family.child?.name
print(name) //Optional("dohyeon") 출력
```

#### 참고
https://zetal.tistory.com/entry/swift-%EA%B8%B0%EC%B4%88%EB%AC%B8%EB%B2%95-4-%EC%98%B5%EC%85%94%EB%84%90