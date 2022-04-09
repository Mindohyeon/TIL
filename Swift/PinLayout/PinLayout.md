# PinLayout
Auto Layout 없이 Swift View 레이아웃을 구성할 수 있도록 도와주는 프레임워크이다.


## PinLayout Style Guide

1. 동일한 순서로 메서드를 정의해야 한다.
- 레이아웃을 더 쉽게 이해할 수 있기 때문이다.
```swift
view.pin. [EDGE | ANCHOR | RELATIVE]. [WIDTH | HEIGHT | SIZE]. [pinEdges ()].[MARGINS]. [sizeToFit ()]
```

이 순서는 PinLayout 내부 로직을 반영한다고 한다.
PinEdges() 는 margins 전에 적용되고, margins 는 sizeToFit() 전에 적용된다.