# 4_TIL_Private

:purple_heart: Java

:green_heart: Python

:black_heart: 인프라

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

## 4/18(금)
:purple_heart: Java Review
- 자바메모리구조 📌
    - 메서드 영역 (static)
    - 스택 영역 (지역 변수)
    - 힙 영역 (new 인스턴스)
        - 힙 영역 안에 인스턴스가 참조하는 곳을 모두 잃게 된 경우 GC가비지컬렉션 대상이 됨
        

## 4/19(토)
:purple_heart: Java Review
- 변수
    - (단독) 인스턴스변수 // 힙영역,GC삭제까지삼 // 동적
    - (공유) static변수, 정적변수, 클래스변수 // 메서드영역,매우오래삼 //정적 
    - 매개변수 // 스택영역,생명짧음 
    - 지역변수 // 스택영역,생명짧음
- static 
    - static 변수 = 정적변수 = 클래스변수
    - static 메서드 = 정적메서드 = 클래스메서드
        - static 안에는 static 쓰기 📌
    - 사용 예) 상수(전역설정값,환경변수,고정URL), 유틸리티 기능, 각 인스턴스에게 고유번호부여 등

## 4/20(일)
:purple_heart: Java Review
- final
    - 상수 public static final CONST_VALUE = 1;
        - 효과) 메서드영역으로 1개만 써서 메모리낭비 줄임, 상수로 고정된 값 사용
    - 참조형변수 final Data data = new Data(); // 객체의 참조값 변경불가 
                [X] data = new Data(); // 컴파일 오류남(불가)
                [O] data.value = 20; //그러나, 그 객체의 내부 값은 변경가능


- 상속
    - 자바 : 단일상속(부모1개) / class 자식 extends 부모
        - 메서드 오버라이딩(Overriding) : 부모 메서드를 자식이 다르게 재정의
            - @Override 어노테이션
            필수 아님(없어도 동작 함), 그러나 붙였는데 부모 메서드 없으면 오류남
            - 조건 📌
                - '[X] 생성자, static, final, private 불가
                - 예외 : 자식이 더 많이 throws 불가
                - 접근제어자 : 자식이 더 제한적인 접근제어자 불가
                - 이름, 매개변수, 반환타입 같아야함

- 오버로딩 vs 오버라이딩
    - 오버로딩 : 과적, 같은이름 메서드의 다른매개변수 ex.계산기
    - 오버라이딩 : 타고오름 상속, 부모기능을 자식이 재정의

- 추상화, 인터페이스  📌
```java
abstract
public abstract class GasCar extends Car
```

## 4/21(월)
:purple_heart: Java Review
- 상속 super
    - super.변수
    - super.메서드()
    - super(...) // 부모 생성자
        - 맨 첫 줄 
        - super() // 기본형 생략가능
        - super(), this() 같이 못 씀 

## 4/22(화)
:purple_heart: Java Review
- 다형성
    - 다형적 참조 : 다양한 형태를 참조할 수 있다.

        - 부모는 자식을 품을 수 있다.
        - 부모 타입의 변수는 자식 타입(하위) 인스턴스 참조할 수 있다.
        - Parent poly = new Child()
        실행) 참조값(주소)을 사용해 인스턴스를 찾는다. 그 안의 실행할 타입 찾는다.
        단, 부모 타입을 찾고(올라갈 수 있음), 자식으로 내려올 순 없음.

## 4/23(수)
:purple_heart: Java Review
- 다형성
    - cast
        - 업캐스팅 
            - 안전 : 인스턴스 내부에 부모가 모두 생생되어있음
            Child child = new Child(); 는 위 상속 다 가지고 생성됨
            1) Parent poly = (Parent) child
            2) Parent poly = child     // 생략가능 권장
             
        - 다운캐스팅 
            - 위험 : 인스턴스 내부에 자식이 없어서 자식만의 정보 못 씀 
            ```
            Parent poly1 = new Child();
            1) Child poly2 = (Child) poly1; (가능) O
            poly2.childMethod() (가능/불가)?
             : 
            Parent parent = new Parent();
            1) Child poly = (Child) parent; (불가!) X
             : 자식은 부모를 품을 수 없다.
            ```

정리
---

### 🔁 다형성 (Polymorphism)
- **부모 타입의 참조변수**로 **자식 객체를 참조**할 수 있음.
- 실제 인스턴스는 자식이지만, 참조는 부모 타입 → 이게 **업캐스팅**

---

### ⬆️ 업캐스팅 (Upcasting)
```java
Child child = new Child();

// 업캐스팅
Parent parent1 = (Parent) child;  // 명시적 캐스팅 (생략 가능)
Parent parent2 = child;          // 암시적 캐스팅
```

- **항상 안전함**: 자식은 부모를 "포함"하므로, 부모 타입으로 변환해도 문제 없음.
- 단, **부모 타입에서 정의된 멤버까지만 접근** 가능함.
```java
parent.parentMethod();   // ✅ 가능
parent.childMethod();    // ❌ 에러! Parent 타입엔 없음
```

---

### ⬇️ 다운캐스팅 (Downcasting)
```java
Parent parent = new Child();  // 업캐스팅된 상태

// 다운캐스팅
Child child = (Child) parent;  // 가능, 실제 인스턴스가 Child라면 OK
child.childMethod();         // 자식 고유 메서드 호출 가능

parent.childMethod();   // ❌ 안 됨 (Parent 타입이라서)
child.childMethod();    // ✅ 다운캐스팅 후 자식 기능 사용 가능
```

- **항상 가능한 건 아님!**  
  - 부모 타입 참조가 실제로 자식 객체를 가리키고 있을 때만 가능함.

```java
Parent parent = new Parent();
Child child = (Child) parent;  // ❌ 런타임 오류(ClassCastException)
```

- 부모 객체는 자식 클래스의 멤버를 갖고 있지 않기 때문에 위험함.

---

### 🧠 핵심 요약
| 캐스팅 종류   | 방향             | 안전성 | 설명 |
|--------------|------------------|--------|------|
| 업캐스팅     | 자식 → 부모       | 안전함 ✅ | 자동 또는 명시적 캐스팅 가능 |
| 다운캐스팅   | 부모 → 자식       | 위험함 ⚠️ | 명시적 캐스팅 필요, 실제 타입 확인 필요 (`instanceof` 등) |

---

필요하면 `instanceof`로 타입 체크 후 다운캐스팅하면 안전:
```java
if (parent instanceof Child) {
    Child child = (Child) parent;
    child.childMethod();
}
```

---

## 4/24(목)
:purple_heart: Java Review
- 다형성
    - 다형적 참조 : 부모 타입의 변수는 자식 타입(하위) 인스턴스 참조할 수 있다.
    - 메서드 오버라이딩 : parent.메서드() 해도 @Override child.메서드() 있으면, 오버라이딩된게 우선순위

다형성 왜 필요할까? 퉁쳐서 쓸 필요가 있어서 (ex.Object, print())

- 추상화 abstract :**제약** 걸어주기
    - 추상화 클래스: 인스턴스 생성 못함
    - 추상화 메서드: 자식클래스에 꼭 @Override 해야 할 메서드 명시

- 순수 추상 클래스 (모두 추상화) => 인터페이스 

- 인터페이스 interface
    - 메서드 public abstract 생략 권장
    - 멤버 변수 public static final 생략 권장
    - 다중 **구현**(상속) 가능
    - implements
    - 특이사항 )
        - 자바8 interface의 default 메서드 구현가능
        - 자바9 interface의 private 메서드 구현가능

- 클래스 vs 인터페이스

## 4/25(금)
DRY : Do not Repeat Yourself

:green_heart: Python Review

도구 : https://jupyter.org/try-jupyter/lab/
자료 : 점프 투 파이썬 https://wikidocs.net/book/1

연산(데이터 타입에 따름), 함수, 제어문(반복문,조건문)

자료구조 : 리스트, 딕셔너리, 튜플, 셋

공통 : 데이터 꺼낼 때 대괄호[] 사용
.(dot)

함수 ()
리스트 []
딕셔너리 {}
    - 딕셔너리 = {'키값':value, '키값':value, ...}
    - 딕셔너리['키값'] = 데이터 

함수
-print()
-sum([1],2) 
*주피터노트북에서 함수 끝에 shift+tap 하면 함수 쓰는 법 나옴 

반복문
1) for문
for 변수 in 순서있는 자료구조 :
    반복할 코드

2) while문 - 조건이 참일 동안 반복
while 조건 : 
    반복할 코드
