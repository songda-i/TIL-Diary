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
 
## 5/3(토)
:purple_heart: Java Review