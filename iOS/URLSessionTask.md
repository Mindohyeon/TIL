# URLSessionTask
URLSessionTask 는 특정 리소스 다운로드 같이 URLSession 에서 수행되는 task 를 의미한다.

## URLSessionTask 의 자식 클래스
- URLSessionDataTask
- URLSessionDownloadTask
- URLSessionUploadTask

### URLSessionDataTask
URLSessionDataTask 는 다운로드한 데이터를 JSONData 타입의 object 로 넘겨주는 task 를 의미한다.

서버에서 메모리로 데이터를 검색하는 HTTP GET 요청에 이 Task 를 사용한다.

### URLSessionDownloadTask
URLSessionDownloadTask 는 서버에서 응답으로 준 데이터를 파일에 저장해주는 task 를 의미한다.


### URLSessionUploadTask
URLSessionUploadTask 는 ```URLSessionDataTask``` 를 <b>상속</b>하고 있고, 데이터를 request body 에 넣어서 서버에 업로드하는 task 를 의미한다.