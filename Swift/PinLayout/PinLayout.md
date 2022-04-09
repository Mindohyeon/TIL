# PinLayout
Auto Layout 없이 Swift View 레이아웃을 구성할 수 있도록 도와주는 프레임워크이다.


## PinLayout Style Guide

##### 1. 동일한 순서로 메서드를 정의해야 한다.
   - 레이아웃을 더 쉽게 이해할 수 있기 때문이다.
```swift
view.pin. [EDGE | ANCHOR | RELATIVE]. [WIDTH | HEIGHT | SIZE]. [pinEdges ()].[MARGINS]. [sizeToFit ()]
```

이 순서는 PinLayout 내부 로직을 반영한다고 한다.
PinEdges() 는 margins 전에 적용되고, margins 는 sizeToFit() 전에 적용된다.

##### 2. Edges 는 항상 순서대로 명시해야 한다. (Top, Bottom, Left, Right 순서)
```swift
view.pin.top().bottom().left(20%).right(20%)
```

##### 3. 레이아웃 라인이 길어지면 라인을 분리해야 한다.
```swift
textLabel.pin.below(of: titleLabel)
    .before(of: rightTextlabel).after(of: afterTextLabel) 
    //above 는 뷰의 가장 아래쪽에 위치한다. 이걸 제일 아래로 두고 아래서부터 쌓는 느낌
    .above(of: button).marginHorizontal(10)
```