# 주석

## Xml 에서의 주석 

- <> 안쪽에 주석을 작성할 경우 오류가 발생한다.

### 방법
```
<!-- 주석처리 하고 싶은 말 -->
```

#### 옳은 주석 방법
  
```kotlin
<ScrollView
        android:layout_width="match_parent"
        android:layout_height="match_parent">
        <!-- 여기는 오류가 아님!! -->

    <LinearLayout
```

#### 옳지 않은 주석 방법
```kotlin
<ScrollView
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        <!--여기는 오류가 발생!! -->>
```


## Activity 에서의 주석 방법

### 한 줄을 주석처리 할 경우

#### 방법
```
// 주석처리 하고 싶은 말
```

### 여러 줄을 주석처리 할 경우

#### 방법
```
/* 주석처리 하고 
싶은 말*/
```

### 단축키

#### 한 번에 여러 줄을 주석처리 할 때
```Ctrl + /```   
<b>Microsoft 입력기 상태일 때만 가능</b>



