# View Binding 이란?
view 와 상호 작용할 때 코드를 쉽게 작성할 수 있게 지원해준다.

findViewById 를 쓰지 않고 컴포넌트를 접근할 수 있게 도와준다.



# View Binding 설정하기

build.gradle(module.app) 에 viewBinding 요소 추가하기
```kotlin
android{
    ---
    buildFeatures {
        viewBinding = true

    }
}
```
Sync Now 를 눌러 적용한다.

<b>MainActivity.kt</b>

이처럼 이름 뒤에 Binding 이라고 써주면 된다.

```kotlin
class MainActivity : AppCompatActivity() {
    private lateinit var binding: ActivityMainBinding
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        binding = ActivityMainBinding.inflate(layoutInflater)
        val view = binding.root
        setContentView(view)
    }
}
```

## findViewById 와 차이점
- Layout 파일과 실제 Java/Kotlin 코드간에 일치하지 않기 때문에 더 빠르게 에러를 잡을 수 있고, 생산성을 늘릴 수 있다.