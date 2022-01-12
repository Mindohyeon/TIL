# MARK: - 란?
같은 파일 내에서 직접적인 관련이 있는 부분끼리 서로 묶어주는 <b>구역설정의 방법</b>

구분선이 생기며 Xcode 내부에서도 따로 관리해준다.

## 왜 필요할까?
MVC 패턴이나 delegate 패턴으로 분리하더라도, 한 파일에서 코드가 길어질 수 있다.

코드가 밑으로 길어지면 <b>가독성이 떨어진다.</b>

코드의 흐름마저 분리하지 않고 섹션을 구분하는 방법이 바로 ```MARK: -``` 방법이다.

1. (주석기호) //을 적는다
2. 그 옆에 MARK: - 를 적는다.
3. 한 칸을 띄고 표시하고 싶은 구역을 적는다.

```swift

//MARK: - Protocol1
protocol Protocol1 {
    func func1()
}

extension Protocol1 {
    func func1() {
        print("extension Protocol1")
    }
}

```