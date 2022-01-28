# dequeueReusableCell 이란?
지정된 재사용 식별자에 대한 재상요 가능한 테이블 뷰 셀 객체를 반환하고, 이를 테이블에 추가한다.

```swift
let cell = tableView.dequeueReusableCell(withIdentifier: "cell", for: indexPath)
```

### identifier
여기에서 재사용 식별자는 withIdentifier 가 된다.

여기에는 위에 쓴 "cell" 처럼 String 이 들어간다.
이는 재사용할 객체를 나타내는 문자열이 된다.
그리고 반드시 <b>nil</b>이면 안 된다.

#### 정리
<b>지정해주는 String 형 identifier 는 재사용할 객체를 나타내준다.</b>

### for
위를 보면 indexPath 를 받고 있다.
```swift
func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
            let cell : UITableViewCell = tableView.dequeueReusableCell(withIdentifier: "cell", for: indexPath)
        
        cell.textLabel?.text = "Cell : \(indexPath.row)"
        
        return cell
}
```

indexPath는 tableView 메서드 안에 있었다.
tableView 는 UITableView 와 IndexPath 를 받는다.
받은 IndexPath 를 indexpath라고 해준거다.

#### for 파라미터에서의 indexpath 의 역할
<b>셀의 위치를 지정</b>하는 indexPath 이다.
데이터 소스는 셀에 대한 요청이 있을 때 정보를 수신하며 이를 전달해야 한다. 이 방법은 index 경로를 사용하여 tableView에서 셀의 위치를 기반으로 추가 구성을 수행한다.

---
## 사용하는 이유
<b>메모리를 줄이기 위해서이다.</b>