# 4_TIL_Private

:purple_heart: Java

:green_heart: 인프라 - AWS

:handshake: PJT업무

:crescent_moon: 달이 조언​

:heart: 개념/용어

:blue_heart: 글/영상

:books: 책/강의

---

## 4/11(금)
:purple_heart: Java Review

- List
    - ArrayList
        - 검색(읽기)용   
    - LinkedList
        - 추가/삭제용

## 4/12(토)
:purple_heart: Java Review

- 생성자
    - 기본생성자, 오버로딩, this. ,this()
- 출력
    - System.out.println() : 문자열을 단순히 출력하는 메서드.
      포맷팅 기능을 직접 지원하지 않음
      두 번째 매개변수를 전달하려고 하면 컴파일 오류 발생
    - System.out.printf() : 포맷팅 기능을 직접 지원
- 패키저
    - import
- 접근제어자(access modifier)
    - 폐쇄 private -> default -> protected -> public 개방
    - 모든 외부 호출 
        - 막는다 (private)
        - 허용한다 (public)
    - 일부 허용
        - 같은 패키저 안에만 허용한다 (default = package-private)
        - 같은 패키저 안에만 허용하고 , 패키저 달라도 상속관계면 허용한다 (protected)

## 4/16(수)
:purple_heart: Java Review
- 캡슐화 : 속성과 기능을 하나로 묶고, 필요한 기능만 외부로 노출하고 나머지는 내부로 숨긴다.
- 클래스 레벨 접근 제어자
    - public : 클래스명과 파일명 이름 동일, 1개만 등장
    - default : N개 가능

## 4/18(목)
:purple_heart: Java Review
- 자바메모리구조
    - 메서드 영역 (static)
    - 스택 영역 (지역 변수)
    - 힙 영역 (new 인스턴스)
        - 힙 영역 안에 인스턴스가 참조하는 곳을 잃게 된 경우 GC가비지컬렉션 대상이 됨