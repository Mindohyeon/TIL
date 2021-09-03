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
