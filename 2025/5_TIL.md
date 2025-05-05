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

- 자바 데이터 타입
    - 기본형(Primitive Type) : 공유X
    - 참조형(Reference Type) : 공유O

- 가변(Mutable) 객체 vs 불변(Immutable) 객체
    - 가변 객체
    - 불변 객체 : `final` 값을 변경할 수 없게 함
        - 주의 ) 불변 객체에서 변경과 관련된 메서드들은 보통 객체를 새로 만들어서(new) 반환하기 때문에 , 꼭 반환값을 받아야한다.
        - 예 )  String, Integer, LocalDate 등 클래스
        - 이유 ) 캐시 안정성, 멀티 쓰레드 안정성, 엔티티의 값 타입