# URLSession 
iOS 앱에서는 서버와 통신하기 위해 애플은 ```URLSession``` 이라는 API를 제공하고 있다.
URLSession 은 HTTP / HTTPS 를 포함한 몇 가지 프로토콜을 지원하고, 인증, 쿠키 관리, 캐시 관리 등을 지원한다.

## URLSession의 Request 와 Response
URLSession 은 다른 HTTP 통신과 마찬가지로, Request 와 Response 를 기본 구조로 가지고 있다.

#### Request
Request는 URL 객체를 통해 직접 통신하는 형태와, URLRequest 객체를 만들어서 옵션을 설정하여 통신하는 형태가 있다.

#### Response
Response는 설정된 ```Task```의 ```Completion Handler``` 형태로 ```response를``` 받거나, ```URLSessionDelegate```를 통해 지정된 메서드를 호출하는 형태로 ```response를``` 받는 형태가 있다.

일반적으로 간단한 response 를 작성할 때에는 ```Completion Handler``` 를 사용하지만, <b>앱이 background 상태로 들어갈 때에도 파일 다운로드를 지원하도록 설정하거나, 인증과 캐싱을 default 옵션으로 사용하지 않는 상황 같은 경우</b>에는 <b>```Delegate``` 패턴을 사용해야 한다.</b>

<b>*Task</b> : swift 가 코드를 병렬로 실행하는 기본 메커니즘. 각 Task 는 다른 Task 와 함께 동시(concurrent)에 실행할 수 있는 새로운 비동기 컨텍스트를 제공한다.
