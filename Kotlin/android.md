# Android
안드로이드에서는 메인 ```thread``` 에서 ```runBlocking``` 을 걸어주면 일정 시간 응답이 없는 경우 ```ANR``` 이 발생하며 앱이 강제 종료된다.

## ANR 이란?
<b>Application Not Responding</b> : 응답 없음 오류


버전 오류가 뜰 때에는 버전 뒤에 + 를 써보자

---
### Hash Key 란?
특정 데이터를 해시 함수에 입력한 결과로 받은 리턴값을 의미한다.

오픈 API(카카오 맵, FCM , Facebook 로그인 등)를 사용하려면 Hash Key 를 등록해야 하고, Key Hash 가 등록된 앱만 SDK 를 이용해 API 를 호출할 수 있다.

- 개발용 key   

<b>개발할 때만 사용하는 키</b>로 안드로이드 개발환경에 기본적으로 저장되어있는 인증서 바이너리에 대한 hash 값

- 릴리즈용 key

<b>실제 앱을 배포할 때 사용</b>하는 인증서 바이너리에 대한 hash 값

---

### hash function 이란?
임이의 데이터를 고정된 길이의 데이터로 매핑하는 함수이다.

- Key Hash는 Hash 함수의 출력값을 말한다.
- 데이터의 길이가 랜덤해도 리턴값의 길이는 일정하다.
- 입력값이 같으면 리턴값도 언제나 동일하다.
- 함수의 출력 값만 갖고 입력값을 추론하는 것은 어렵다.
- API 공급업체에서는 사용자 구분을 위해 Hash 함수의 출력값인 Key Hash를 사용한다.

암호화 된 Key 값이라는 개념으로 보안인증에 사용되곤 한다.

## Key Hash 획득하기

#### 기본 개념
Android Application 은 Java 기반이라 Android 개발 머신에는 JDK 가 설치되어 있다.   
또한, jdk/bin 폴더에 있는 다양한 어플리케이션 중 해시키를 생성할 수 있는 <b>keytool</b> 이라는 프로그램이 들어있다.

---

### android stuido 에서 Java로 코드를 작성할 때 getter 와 setter 단축키

- <b>```Alt``` + ```Insert```</b>


---


## Error running 'MainActivity': The activity must be exported or contain an intent-filter ?


run 버튼 옆에 app이 아닌 서브 액티비티명으로 되어있는지 확인해보자.

## Unreachable statement
도달할 수 없는 명령문이다

return 문이나 무한 루프를 다시 보자