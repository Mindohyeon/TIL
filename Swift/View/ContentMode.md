# ContentMode
UIImageView에 Image 를 넣을 때 어떤 비율로 넣을지 정해야 할 때가 있다.
이때 UIVIew.ContentMode 를 이용하는데 주요 속성을 알아보자.

## UIVIew 의 ContentMode

### scaleToFill
콘텐츠의 비율을 변경하여 View 크기에 맞게 확장하는 옵션

### scaleAspectFit
콘텐츠의 비율을 유지하여 View 크기에 맞게 확장하는 옵션. 남는 영역은 투명해진다.

### scaleAspectFill
콘텐츠의 비율을 유지하여 View 크기에 빈 영역 없이 확장하는 옵션. 일부 내용은 잘라질 수 있다.

<b>Aspect = 비율 유지
Fill = 빈 영역 없이 꽉 채움
Fit = 화면에 맞게</b>