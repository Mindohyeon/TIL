## XML

> <>태그로 감싼 태그요소와 태그 안에서 '항목명 = 값 형식'을 지정하는 속성으로 이루어진다  
+ 되도록이면 처음 시작 태그를 LinearLayout로 시작해야 Layout이 깔끔하다.
+ 드래그로 xml을 만들지 말자  
-> 드래그로 만들면 다른 사람과 공유했을 때 올바르게 실행되지   않는다. 또한 실력이 잘 늘지 않는다.  

## 기준점
- 기준점이 없는 경우
```kotlin
  <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="버튼 1"
        />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="버튼 2"
        />
```
실행할 경우에 버튼 1과 버튼 2가 겹쳐서 보여진다.

- 기준점이 있는 경우
```kotlin
   <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="버튼 1"
        android:id="@+id/btn1"
        />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="버튼 2"
        app:layout_constraintTop_toBottomOf="@+id/btn1"
        />
```
버튼 1이 버튼 2 위로 붙는다.
``` 
버튼1  
버튼2
```
---
## margin 과 padding 의 차이

### margin
부모 레이아웃과 ImageView 위젯에 여백을 가진다.

```kotlin
     <ImageView
        android:layout_width="280dp"
        android:layout_height="230dp"
        android:layout_margin="20dp"
```

### padding
ImageView의 테두리로부터 Image의 사이에 여백을 가진다.
 ```kotlin
     <ImageView
        android:layout_width="280dp"
        android:layout_height="230dp"
        android:padding="20dp"
```

> width = 폭,가로  
> height = 높이  
> weight = 두께,무게  

## AndroidManifest.xml  
manifest = 나타내다, 드러내다  
app -> manifests ->AndroidManifest.xml  

> 해당 어플리케이션에 대한 필수적인 정보들을 안드로이드 시스템에 알려준다.
---
## themes.xml  
> Themes는 앱의 전체 style을 지정한다.  
버튼 등 모든것들의 기본 색이나 사이즈가 나와있다.
+ style tag 아래에 작성시 Title Bar가 삭제된다.
```kotlin
<item name="windowNoTitle">true</item>
```
---
## colors.xml
color의 색을 만들 수 있다.
> 방법
1. 원하는 색 이름을 쓴다
2. #ffffffff(이건 아무거나 적어도 나중에 자동으로 바뀜)로 적고  몇번 째 줄인지 알려주는 곳을 클릭하여 색을 선택한다.
```
<color name="색 이름">#ffffffff</color>
```


```kotlin
    <color name="white">#FFFFFFFF</color>
 ```
 ---
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

## Scrollview
+ 구현하려는 내용의 높이가 실제 화면의 높이보다 클 때 화면을 스크롤할 수 있도록 하기 위해 사용한다. 

> Scrollview를 사용하여 내용을 감싸주면 화면의 크기보다 내용물이 커질 때 스크롤이 가능해진다.  

```kotlin
<Scrollview
    android:layout_width="match_parent"  
    android:layout_height="match_parent">
```  
  <br>
  
## LinearLayout
+ 가로로 정렬할지 세로로 정렬할지 결정한다.
```kotlin
<LinearLayout
    android:layout_width="match_parent"  
    android:layout_height="match_parent">
    android:orientation="vertical" >
</LinearLayout>
```

 orientation = 수평으로 할지 수직으로 할지 방향을 정한다.   
 LinearLayout에 필수적으로 들어가는 요소이다.  

> vertical = 수직  
> horizontal = 수평<br>


## gravity    
- 자식 view들의 중력을 결정한다.

#### layout_gravity 
레이아웃 안에서 어디에 위치할 것인지 정한다.

#### ignoregravity
gravity 설정 상태에서 특정 자식의 view 속성을 무시한다.



## RelativeLayout
- 상대적 위치에 하위 뷰를 표시하는 뷰 그룹이다.

#### layout_centerlnParent
부모 뷰그룹 영역에서 정중앙에 배치된다.

#### layout_alignParentBottom
부모 뷰그룹 영역에서 하단에 배치된다. (왼쪽)

#### layout_alignParentRingt
부모 뷰그룹 영역에서 우측에 배치된다. (상단)

#### layout_alignParentEnd
부모 뷰그룹 영역에서 오른쪽과 해당뷰의 오른쪽을 일치시킨다.

#### layout_centerHorizontal
부모 뷰그룹의 가로 중앙에 배치한다. (상단)

#### layout_centerVertical
부모 뷰그룹의 세로 중앙에 정렬한다. (왼쪽)

#### layout_above
기준이 되는 뷰의 상단에 배치한다. (왼쪽)

#### layout_toRightOf
기준이 되는 뷰의 오른쪽에 배치한다. (상단)

#### layout_below
기준이 되는 뷰 하단 아래쪽에 배치한다.

#### layout_toLeftOf
기준이 되는 뷰 좌측의 왼쪽에 배치한다.




  
  
## Button
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

## EditText
+ 사용자가 텍스를 입력할 수 있는 기능을 제공한다.
android:hint="어떤 걸 입력해야 할지"  
hint = 이 부분에 어떤 텍스트를 입력해야 할지 알려줄 수 있다.
```kotlin
<EditText
    android:layout_width="180dp"
    android:layout_height="wrap_content"
    android:gravity="center"
    android:hint="입력해주세요.">

</EditText>
```

## ImageView
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
+ 가끔 오류 발생시 대부분의 이유
1. drawable 이 아닌 v-24로 이미지가 들어가 있는 경우  
-> project로 들어가서 v-24에 들어가 있는 이미지를 drawable로 이동시킨다.
2. 이미지 이름을 대문자 등으로 작성할 경우  
-> 웬만하면 영어로 소문자만 쓰자  

## ImageButton
+ Image를 버튼처럼 사용할 수 있다.
+ backgroundcolor를 흰색으로 바꾸면 버튼의 색이 보이지 않아 자연스럽게 보인다.
```kotlin
<ImageButton
    android:id="@+id/rainbutton"
    android:layout_width="266dp"
    android:layout_height="229dp"
    android:layout_marginTop="225dp"
    android:layout_marginStart="68dp"
    android:src="@drawable/logo"
    android:background="@color/white"/>
```

## FrameLayout
+ 여러 개의 뷰를 중첩으로 배치할 수 있게 해준다.

#### 방법
1. FrameLayout 안에 중첩시킬 뷰를 넣는다.
2. 가장 앞에 보일 뷰를 가장 아래에 배치시킨다.


```Kotlin
<FrameLayout
    android:layout_width="wrap_content"
    android:layout_height="wrap_content">
</FrameLayout>
```

## Viewpager
- 화면을 페이지처럼 좌우로 넘길 때 사용되며, 페이지의 생명주기를 관리하기 위해 ```Fragment```와 함께 쓰이는 경우가 대부분이다.

















