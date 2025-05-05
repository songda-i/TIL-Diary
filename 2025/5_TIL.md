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
    - 문자열 비교는 `equals()`메서드 사용
    - 동일성(Identity) : 물리적, `==`연산자 / 사용 X
        - " " 문자열 리터럴 일 때, `문자열 풀 Pool` 사용으로 같게 됨
    - 동등성(Equality) : 논리적, `equals()`메서드 / 사용 O
        - " ", new String(" ") 둘 다 같게 됨
* Pool
    - 풀 : 공용 자원 모아둔 곳
    - 문자열 풀은 힙 영역을 사용
    - 문자열 풀에서 문자를 찾을 때 `해시 알고리즘`을 사용하기 때문에 매우 빠른 속도

- String 클래스 특징
    - 불변객체
        - str2 = str1.concat("")
        변경이 필요한 경우 기존 값을 변경하지 않고, 
        대신에 새로운 결과를 만들어서 반환한다

- 메서드 체인닝 - Method Chaining
    - 메서드 호출 결과 =  인스턴스 자기 자신의 참조값(주소)을 반환 return this

- 합치기
    - `+`
    - StringBuilder().append().append()....toString() // 메서드 체이닝
        - 직접 StringBuilder 쓸 때
            - 반복문에서 반복해서 문자를 연결할 때
            - 조건문을 통해 동적으로 문자열을 조합할 때
            - 복잡한 문자열의 특정 부분을 변경해야 할 때
            - 매우 긴 대용량 문자열을 다룰 때

- StringBuilder vs StringBuffer
    - StringBuilder : 빠름
    - StringBuffer : 느림, 멀티스레드에서 안전


