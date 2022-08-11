# DI 란?

Dependency Injection 의 약자로 **의존성 주입**이라는 뜻이다.

### 의존성 주입
의존성 주입은 의존성 + 주입이다.
 즉, 의존관계를 갖도록 외부에서 객체를 생성해서 넣어준다는 뜻이다.

**그러나 의존성을 주입하는 것만으로 의존성 주입이라고 하지 않는다.**

### 의존성 분리
DI 는 **의존성을 분리시켜 사용한다.** 그렇다면 의존성은 어떻게 분리할까?

- 의존성 분리는 **의존성 역전 원칙**으로 의존성을 분리시킨다.

## 의존성 역전 원칙
(Dependency Inversion Principle) 의 약자로 객체지향 프로그래밍 5가지 기본원칙(SOLID) 중 D 에 해당하는 DIP(의존성 역전 원칙) 이다.

> 쉽게 말하면 상위 계층이 하위 계층의 구현으로부터 독립적이어야 한다는 것이다.



#### 참고
- [DI Container](https://eunjin3786.tistory.com/233)
- [DI 란?](https://medium.com/@jang.wangsu/di-dependency-injection-%EC%9D%B4%EB%9E%80-1b12fdefec4f)