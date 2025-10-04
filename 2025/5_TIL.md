# 5_TIL_Private

:purple_heart: Java

:green_heart: Python

:black_heart: 인프라

:handshake: PJT업무

:crescent_moon: 달이 조언​

:heart: 개념/용어

:blue_heart: 글/영상

:books: 책/강의

---

## 5/1(목)
:purple_heart: Java Review

package java.lang (당연해서 import 생략가능)
- 묵시적(Implicit) vs 명시적(Explicit)
    - 묵시적 : 자동으로 함
    - 명시적 : 말해줘야 함

> Object 클래스
- Object 클래스 : 최상위 부모클래스
    - 모든 객체에 필요한 공통 기능 제공, 다형성의 기본구현
        - toString(), equals(), getClass()...
        ```java
        public String toString() {
            return getClass().getName() + "@" + Integer.toHexString(hashCode());
        }
        ```
- 객체의 정보 알아보기 : 참조값 출력
    ```java
    # 1
    # 2 
    # 3
    String ref = Integer.toHexString(System.identityHashCode(dog));
    System.out.println(ref);
    ```

- System.out.println(객체);
해당 객체의 toString() 메서드가 호출됩니다.

1. 만약 toString()을 오버라이드하지 않았다면?
기본적으로 Object 클래스의 toString()이 호출됩니다.

    이때 결과는:
    클래스이름@해시코드(16진수)
    예: lang.wrapper.MyInteger@2f4d3709

2. toString()을 오버라이드했다면?
만약 객체 클래스에서 toString()을 오버라이드했다면,
System.out.println(객체)는 오버라이드된 내용을 출력

## 5/4(일)
:purple_heart: Java Review
> Object 객체의 대표메서드 : toString(), equals()
- toString() : 객체의 문자열 정보
    - println() - 내부에서 toString() 호출하기
    - toString() 오버라이딩해서 사용하기

- 같다
    - 동일성(Identity) : 물리적, `==`연산자, 참조가 동일한 객체를 가르키는지, 완전히 같음
    - 동등성(Equality) : 논리적, `equals()`메서드, 두 객체의 내용물이 같은지, 같은 가치와 수준 의미(형태나 외관이 완전히 같지 않음)

> 불변 객체
- 자바 데이터 타입
    - 기본형(Primitive Type) : 공유X
    - 참조형(Reference Type) : 공유O

- 가변(Mutable) 객체 vs 불변(Immutable) 객체
    - 가변 객체
    - 불변 객체 : `final` 값을 변경할 수 없게 함
        - 주의 ) 불변 객체에서 변경과 관련된 메서드들은
            - 보통 객체를 새로 만들어서(new) 반환하기 때문에 , 꼭 `반환값`을 받아야한다.
            - `with` 시작하는 명칭을 쓴다. 
                "coffee with sugar"
        - 예 )  String, Integer, LocalDate 등 클래스
        - 이유 ) 캐시 안정성, 멀티 쓰레드 안정성, 엔티티의 값 타입

## 5/5(월)
:purple_heart: Java Review
> String 클래스

- 비교
    - 문자열 비교는 `equals()`메서드 사용 ☆
    - 동일성(Identity) : 물리적, `==`연산자 / 사용 X
        - " " 문자열 리터럴 일 때, `문자열 풀 Pool` 사용으로 같게 됨
    - 동등성(Equality) : 논리적, `equals()`메서드 / 사용 O
        - " ", new String(" ") 둘 다 같게 됨
        - 안에 내용물이 같은지가 중요함
* Pool
    - 풀 : 공용 자원 모아둔 곳
    - 문자열 풀은 힙 영역을 사용
    - 문자열 풀에서 문자를 찾을 때 `해시 알고리즘`을 사용하기 때문에 매우 빠른 속도

- String 클래스 특징
    - 불변객체
        - str2 = str1.concat("")
        변경이 필요한 경우 기존 값을 변경하지 않고, 
        대신에 새로운 결과를 만들어서 반환한다

* String (불변) vs StringBuilder (가변)

- StringBuilder - 가변 String
    - 성능 최적화 : 새로운 객체를 만들지 않음 
    - 삽삭갱뒤집기 append(), insert(), delete(), reverse() 등
    - toString 메소드를 사용해 StringBuilder의 결과를 기반으로 String을 생성해서 반환
        - 메서드 체인닝 - Method Chaining
            - ex. StringBuilder().append().append()....toString()
        - 메서드 호출 결과 =  인스턴스 자기 자신의 참조값(주소)을 반환 return this
    - 직접 StringBuilder 쓸 때 (최적화)
        - 반복문에서 반복해서 문자를 연결할 때
        - 조건문을 통해 동적으로 문자열을 조합할 때
        - 복잡한 문자열의 특정 부분을 변경해야 할 때
        - 매우 긴 대용량 문자열을 다룰 때

* StringBuilder vs StringBuffer
    - StringBuilder : 빠름
    - StringBuffer : 느림, 멀티스레드에서 안전
        - list의 Vector

> 래퍼(Wrapper) 클래스 : 기본형의 객체 버전
- 기본형 vs 래퍼클래스
    - 기본형(Primitive Type)은 데이터조각임 : 객체 아님. 메서드 없음. null값 없음
    - 특정 기본형을 감싸서(Wrap) 만든 클래스를 래퍼 클래스 : 객체임

        | 기본형 (Primitive Type) | 래퍼 클래스 (Wrapper Class) |
        | -------------------- | ---------------------- |
        | `byte`               | `Byte`                 |
        | `short`              | `Short`                |
        | `int`                | `Integer`              |
        | `long`               | `Long`                 |
        | `float`              | `Float`                |
        | `double`             | `Double`               |
        | `char`               | `Character`            |
        | `boolean`            | `Boolean`              |

        - 자바는 기본형에 대응하는 래퍼 클래스를 기본으로 제공
        - 기본 래퍼 클래스 특징 : 불변, `equals()` 로 비교해야 한다.

## 5/6(화)
:purple_heart: Java Review
> Eunm 열거 (enumeration)
- 비교 : `==` 사용 
    - `equals()` 비추

* 타입 안전 열거형 패턴 (Type-Safe Enum Pattern)
    ```java
    public class ClassGrade {
        public static final ClassGrade BASIC = new ClassGrade();
        public static final ClassGrade GOLD = new ClassGrade();
        public static final ClassGrade DIAMOND = new ClassGrade();
        //private 생성자 추가 : new 인스턴스 외부 생성 불가
        private ClassGrade() {}
    }
    ```
* 열거형(Enum Type)
    ```java
    public enum Grade {
        BASIC, GOLD, DIAMOND
    }
     ```
    ```java
    import java.lang.Enum

    public class Grade extends Eunm{
        public static final Grade BASIC = new Grade();
        public static final Grade GOLD = new Grade();
        public static final Grade DIAMOND = new Grade();
        //private 생성자 추가
        private Grade() {}
    }
    ```
- 장점
    - 데이터 일관성 및 타입 안정성 : 정해진 값만 사용
    - 확장성 : EUNM 새로운 상수 추가
    - 간결성 : `static import` ?
    - switch문 사용가능 ?

## 5/7(수)
:purple_heart: Java Review
> 날짜와 시간

## 5/8(목)
:purple_heart: Java Review
> 중첩(Nested)클래스, 내부(Inner)클래스

**중첩(Nested)클래스** : 클래스 **안**의 클래스가 있는 것

중첩 클래스는 총 4가지, 크게 2가지로 분류
- 1) 정적 중첩 클래스① 
- 2) 내부 클래스
    - 종류
        - ② 내부 클래스 : -
        - ③ 지역 클래스 : 함수 안 위치
        - ④ 익명 클래스 : 함수 안 위치, 이름없음

| 구분             | static 여부 | 바깥 클래스에 소속 여부 | 비유 표현              |
|------------------|-------------|---------------------------|------------------------|
| 정적 중첩 클래스 | 있음 (O)    | 소속 안 됨 (X)            | 내 안의 다른 것        |
| 내부 클래스      | 없음 (X)    | 소속 됨 (O)               | 내 안의 나             |


※ 실무에서는, `중첩 = 내부` 같이 말함

## 5/14(수)
:purple_heart: Java Review

인스턴스 생성 : new `바깥 클래스.중첩클래스`()
클래스 이름(getClass()) : 바깥 클래스$중첩클래스

중첩클래스는, 같은 클래스에 있으니 
- 캡슐화 가능
- `static` 정적 중첩 클래스의 활용하면 
    - 바깥 클래스의 인스턴스 멤버 접근 불가 [X] 
    - 바깥 클래스의 클래스 멤버(static)에는 접근 가능[O] 
        - `private` 접근 제어자에 접근 가능.
    ```java
        NestedOuter outer = new NestedOuter();
        NestedOuter.Nested nested = new NestedOuter.Nested();
    ```
- 내부 클래스의 활용하면 
    - 바깥 클래스의 인스턴스 멤버 접근 가능[O] 
        - `private` 접근 제어자에 접근 가능.
    - 바깥 클래스의 클래스 멤버(static)에는 접근 가능[O] 
        - `private` 접근 제어자에 접근 가능.
    - **소속**된다 : 바깥클래스의 인스턴스 멤버에는 접근할 수 있으므로, 관련되서 생성해야 함
    
    ```java
        InnerOuter outer = new InnerOuter();
        InnerOuter.Inner inner = outer.new Inner();
        // - 바깥클래스의 인스턴스 참조.new 내부클래스() 로 생성
        // InnerOuter.Inner inner = new InnerOuter.Inner(); // 컴파일오류
    ```
## 5/15(목)
:black_heart: AWS Summit 2025 Seoul

## 5/17(토)
:purple_heart: Java Review
> 예외처리

![alt text](IMAGE/5_TIL_image.png)


체크예외 : 컴파일러 체크, 명시적 처리 필요
언체크예외 (런타임 예외) : 명시적 처리 불필요

주의) Error 시스템 예외는 잡지 않기. Throwable 잡지 않기

예외는 폭탄 돌리기 
- 예외가 발생하면 잡아서 처리하거나, catch
- 처리할 수 없으면 (위)밖으로 던져야한다. throws

## 5/18(일)
:purple_heart: Java Review

> 중첩(Nested)클래스, 내부(Inner)클래스

실무) 중첩은 `static` 클래스만 쓰기 (권장)

```java
// 내부클래스
public class Car {

    private String model;
    private int chargeLevel;
    private Engine engine;

    public Car(String model, int chargeLevel) {
        this.model = model;
        this.chargeLevel = chargeLevel;
        this.engine = new Engine();
    }
    public void start() {
        engine.start();
        System.out.println(model + " 시작 완료");
    }
    // 내부클래스
    private class Engine {
        private void start() {
            System.out.println("충전 레벨 확인: " + chargeLevel);
            System.out.println(model + "의 엔진을 구동합니다.");
        }
    }
}
```

```java
//  중첩(Nested)클래스 (static 변형 권장)
public class Car {

    private String model;
    private int chargeLevel;
    private Engine engine;

    public Car(String model, int chargeLevel) {
        this.model = model;
        this.chargeLevel = chargeLevel;
        this.engine = new Engine(this);
    }
    public void start() {
        engine.start();
        System.out.println(model + " 시작 완료");
    }
    //  중첩(Nested)클래스
    private static class Engine {
        private Car car;
        public Engine(Car car) {
            this.car = car;
        }
        private void start() {
            System.out.println("충전 레벨 확인: " + car.chargeLevel);
            System.out.println(car.model + "의 엔진을 구동합니다.");
        }
    }
}
```

## 5/19(월)
:purple_heart: Java Review

지역 변수 캡처 : 
- 지역 클래스의 인스턴스를 생성하는 시점에, 
필요한 지역 변수를 복사해서 생성한 인스턴스에 함께 넣어둔다
- 지역 클래스가 접근하는 지역 변수의 값은 변경하면 안된다 (사실상 `final`)
    - java: local variables referenced from an inner class must be final or effectively final
    내부 클래스에서 참조되는 지역 변수는 final이거나 사실상(final처럼) 변하지 않아야 한다.

변수의 생명주기


| 메모리 영역    | 변수 유형                     | 생명 주기          | 특징 |
|--------------|----------------------------|------------------|------|
| **메서드 영역** | `static` 변수(클래스 변수)  | 프로그램 종료까지 | 클래스 로딩 시 할당되며, 모든 객체가 공유 |
| **스택 영역**  | 지역 변수, 매개 변수         | 메서드 실행 동안   | 메서드가 호출될 때 생성, 종료되면 제거됨 |
| **힙 영역**   | 인스턴스, 인스턴스 변수      | GC(Garbage Collection) 전까지 | 동적으로 생성되며, 객체가 참조되지 않으면 GC에 의해 제거됨 |

## 5/20(화)
:purple_heart: Java Review

익명 클래스(anonymous class) : 선언 생성 동시에
- 부모클래스 상속 받거나, 인터페이스 구현
- 특징
    - 장점) 간결함
    - 단점) 재사용불가(인스턴스 1회용)

```java

부모클래스/인터페이스이름 인스턴스이름 = new 부모클래스/인터페이스이름() {클래스내용 Body} 
```

## 5/25(일)
:purple_heart: Java Review
> 제네릭(Generic) `<T>`

- 제네릭 타입 : 제네릭 클래스, 제네릭 인터페이스
    - 타입 : 기본형, 클래스, 인터페이스

- 제네릭을 쓰는 이유
    - 타입 안정성
    - 코드 재사용 

```java
// 제네릭 클래스 정의
class GenericBox<T>

// new 객체 생성 : 제네릭의 타입을 선언 `결정`
new GenericBox<Integer>()

// 제네릭 변수 선언 = new 객체 생성<>
GenericBox<Integer> integerBox1 = new GenericBox<Integer>() // 타입 직접 입력
GenericBox<Integer> integerBox2 = new GenericBox<>(); // 타입 추론 (생략 가능) // 권장
GenericBox integerBox3 = new GenericBox();  // Raw Type 원시타입
```

- 용어
    - 메서드는 `매개변수`에 `인자`를 전달해서 사용할 값을 결정한다.
    - 제네릭 클래스는 `타입 매개변수`에 `타입 인자`를 전달해서 사용할 타입을 결정한다.
        - 타입 매개변수 : `<T>`의 T (T말고 어떤 글자든 OK) 
            - 제네릭의 타입 매개변수는 사용할 타입에 대한 `결정`을 나중으로 미루는 것
            -  해당 클래스를 실제 사용하는 생성 시점에, 내부에서 사용할 타입을 결정하는 것
        - 타입 인자 : 실제 타입
            - 기본형 X (int, double ...)
            - 래퍼클래스 O (Integer, Double, String ...)

- Raw Type 원시타입 : 옛 자바 하위 호환용, 내부 타입 변수가 Object 사용됨

## 5/26(월)
:purple_heart: Java Review
> 제네릭(Generic) `<T>`
- 타입 매개변수 제한  `<T extends 특정클래스(상한)>`
    - 매개변수 체크 가능 (컴파일 오류 발생해줘서)
    - 반환값을 다운캐스팅 안해도 됨

## 5/27(화)
:purple_heart: Java Review
- 제네릭 타입
    - 정의: `GenericClass<T>`
    - 타입 인자 전달: 객체를 생성하는 시점
        - 예) `new GenericClass<String>`

- 제네릭 메서드
    - 정의: `<T> T genericMethod(T t)`
    - 타입 인자 전달: 메서드를 호출하는 시점
        - 예) `GenericMethod.<Integer>genericMethod(i)`
        - 타입 추론 가능 `GenericMethod.genericMethod(i)`
    - 사용: 제네릭 메서드는 클래스 전체가 아니라 특정 메서드 단위로 제네릭을 도입할 때 사용
    - 반환타입 : 메서드명 바로 왼쪽 T1

## 5/28(수)
:purple_heart: Java Review

🎯 주의 깊게 봐야 할 자바 핵심 버전
Java 5: 제네릭, 오토박싱, Enum → 현대 자바의 시작
Java 8: 람다, 스트림 → 패러다임 전환
Java 11: LTS, Java 8 다음으로 가장 많이 쓰인 안정 버전
Java 17: 최신 안정 LTS, 기업에서 많이 전환 중
Java 21: 최신 LTS + 가상 스레드 → 서버 성능 혁신 가능

> 컬렉션 프레임워크 