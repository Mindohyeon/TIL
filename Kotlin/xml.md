## XML

> <>태그로 감싼 태그요소와 태그 안에서 '항목명 = 값 형식'을 지정하는 속성으로 이루어진다  
+ 되도록이면 처음 시작 태그를 LinearLayout로 시작해야 Layout이 깔끔하고, 다른 사람과 공유했을 때도 올바르게 실행된다.

> width = 폭,가로  
> height = 높이  
> weight = 두께,무게  

## AndroidManifest.xml  
manifest = 나타내다, 드러내다  
app -> manifests ->AndroidManifest.xml  

> 해당 어플리케이션에 대한 필수적인 정보들을 안드로이드 시스템에 알려준다.

## themes.xml  
> Themes는 앱의 전체 style을 지정한다.  
버튼 등 모든것들의 기본 색이나 사이즈가 나와있다.
+ style tag 아래에 작성시 Title Bar가 삭제된다.
```kotlin
<item name="windowNoTitle">true</item>
```


### 주석
+ <> 밖에 주석을 작성할 경우 오류가 발생하지 않음
> 옳은 주석 방법
```kotlin
<ScrollView
        android:layout_width="match_parent"
        android:layout_height="match_parent">
        <!-- 여기는 오류가 아님!! -->

    <LinearLayout
```
+ <> 안에 주석을 작성하지 않을 경우 오류 발생
>틀린 주석 방법
```kotlin
<ScrollView
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        <!--여기는 오류가 발생!! -->>
```
---
## 태그 종류

### 1.  Scrollview
+ 구현하려는 내용의 높이가 실제 화면의 높이보다 클 때 화면을 스크롤할 수 있도록 하기 위해 사용한다. 

> Scrollview를 사용하여 내용을 감싸주면 화면의 크기보다 내용물이 커질 때 스크롤이 가능해진다.  

```kotlin
<Scrollview
android:layout_width="match_parent"  
android:layout_height="match_parent">
```  
  <br>
  
### 2. LinearLayout
+ 스크롤을 가로로할지 세로로할지 정함
```kotlin
<LinearLayout
android:layout_width="match_parent"  
android:layout_height="match_parent">
android:orientation="vertical" >
</LinearLayout>
```

> orientation = 수평으로 할지 수직으로 할지 정한다.  
vertical = 수직  
horizontal = 수평<br>
  
  
### 3.  Button
+ 버튼을 만든다 

```kotlin
<Button
        android:id="@+id/button2"
        android:layout_width="match_parent"
        android:layout_height="400dp"
        android:text="Button2" />
```
> + button 의 id를 만들어줘야 불러올 수 있음
> + width와 height로 크기를 설정
> + 나타낼 text를 작성

### 4. ImageView
+ 이미지를 띄워준다.
 >#### 방법
 1. drawable에 띄우고 싶은 사진을 드래그해 넣는다.
 2. 띄우고 싶은 xml에 ImageView를 만들고   
 android:src="@drawable/이름">을 입력하면 이미지가 화면에 보인다.

 ```kotlin
     <ImageView
        android:layout_width="280dp"
        android:layout_height="230dp"
        android:layout_marginStart="60dp"
        android:layout_marginTop="240dp"
        android:src="@drawable/logo"/>
```  

### 5. FrameLayout
+ 여러 개의 뷰를 중첩으로 배치할 수 있게 해준다.

> ### 방법
1. FrameLayout 안에 중첩시킬 뷰를 넣는다.
2. 가장 앞에 보일 뷰를 가장 아래에 배치시킨다.


```kotlin
    <FrameLayout
        android:layout_width="wrap_content"
        android:layout_height="wrap_content">
    </FrameLayout>
```













