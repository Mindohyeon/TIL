# dequeueReusableCell 이란?
지정된 재사용 식별자에 대한 재상요 가능한 테이블 뷰 셀 객체를 반환하고, 이를 테이블에 추가한다.

```swift
let cell = tableView.dequeueReusableCell(withIdentifier: "cell", for: indexPath)
```
여기에서 재사용 식별자는 withIdentifier 가 된다.