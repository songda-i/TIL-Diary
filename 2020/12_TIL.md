# 12_TIL_Diary

:apple: 진짜 긍정은 내 삶에서 내가 할 수 있는 일을 하는 것

:purple_heart: Java

[인프런-스프링입문_김영한](https://www.inflearn.com/course/%EC%8A%A4%ED%94%84%EB%A7%81-%EC%9E%85%EB%AC%B8-%EC%8A%A4%ED%94%84%EB%A7%81%EB%B6%80%ED%8A%B8#)

:green_heart: Python

:black_heart: Javascript

:handshake: PJT

:heart: 개념/용어

:blue_heart: 글/영상



## 12/03(목)

:purple_heart: Java  https://www.inflearn.com/course/스프링-입문-스프링부트#

- 인텔리제이, gradle 사용
  - https://start.spring.io/
  - tomcat 웹서버
  - 로그



## 12/04(금)

- 

```
\alley-signal>docker-compose up

\alley-signal\src\main\resources\static\style>sass --watch style.scss style.css
```



## 12/10(목)

 :purple_heart: Java 핵심 용어 한 줄 정리

- 추상클래스 vs 인터페이스
  - 인터페이스(빈 통) : 하위클래스에서 인터페이스의 비어있는 메서드를 반드시 구현해서 사용. 다중상속 가능
  - 추상클래스 : 메서드 안에 일부는 존재하고 일부는 존재하지 않음
  - 공통점 : 그 자체로 인스턴스 선언 할 수 없음. 상속받아 사용함
- 컬렉션 프레임워크
  - List, Set, Map
  - ![img](https://t1.daumcdn.net/cfile/tistory/99B88F3E5AC70FB419)
- 오버로딩 vs 오버라이딩
  - 오버라이딩 : 부모클래스에서 상속받은 메서드를 자식클래스에서 재정의해서 사용하는 것
  - 오버로딩 : 같은 이름의 메서드여도 매개변수의 자료형이나 개수에 따라 다르게 사용하는 것
- 제네릭 : 인스턴스를 선언할 때 자료형이 결정되는 것



## 12/11(금)

:black_heart:  Javascript 심화

    //// JS 는 OOP 객체지향언어이다.
    //// JS의 객체는 키:값 으로 이루어진 {} 이다.
    ////파이썬의 객체는 인스턴스이다.
      
    // 메소드 => 객체안에 정의된 함수 (객체.methodName() 으로 실행하는 함수)
    // 함수 => 메소드 가 아닌 모든 함수
    
    // this 는 기본적으로 window 다.
    
    // 단! 아래의 2가지 경우만 제외하고.
    // 1. method 정의 블록 안의 this -> this는 해당 method 가 정의된 객체(object)
    //    (method 정의 할 때는 arrow function으로 쓰지 않는다!!!)
    // 2. 생성자 함수 안의 this
- AJAX((Asynchronous JavaScript and XML, 에이잭스)) : 브라우저가 가지고있는 (XHR)XMLHttpRequest 객체를 이용해서 전체 페이지를 새로 고치지 않고도 페이지의 일부만을 위한 데이터를 로드하는 기법

* JS의 브라우저 환경이 싱글 스레드 (노동자가 한명) :information_desk_person:

* Blocking (함수가 끝날 때 까지/응답이 도착할 때 까지 기다린다.)

* non-blocking 한 비동기 작업을 한다 => 콜백을 쓸 수 밖에 없도록 설계되어 있다.

  * callback function(콜백 함수) : 함수를 인자로, 실행은 다음에 하기, 함수는 익명으로 가능
    즉, 함수의 인자(괄호) 안에 들어가 있는 함수 (에로우펑션()=>{} this가 vue )

* 순서주의 ) 무작정 막 기다리면 브라우저가 뻗기 때문에 , JS 는 안 기다리고, 최우선 순위 메인을 다 끝낸 후, 그 때 후순위를 한다.

  * 외부 요청 (XHR) - 비동기 요청은 답이 와야 해서 기다리기
  * 기다리기 (settimeout) - 그저 시간이 필요해서 기다리기 

  

* Promise 는 왜 사용하는가 ? 불확실하고 기다려야하는 작업(AJAX axios)을 비동기적으로 처리하기 위해서

* **자바스크립트 함수 특징** : First class function★★★  .ex) number의 1은 

  1 함수를 **인자**로 전달 가능함:star2:     .ex) add(1)

  2 함수를 **반환**할 수 있음:star2: 			.ex) return 1

  3 변수에 함수를 **할당** 가능함:star2: 	.ex) var a =1

  위의 조건은, 프로그래밍 언어에서의 **일급 객체**(first class boject/ first class citizen)의 조건

---

:black_heart:  Javascript 문법

// 변수 선언 정리 (ES6 이전에 var 사용, 지금은 let과 const를 주로 사용)
// var : 할당 및 선언 자유(함수 스코프)
// let : 할당 자유, 선언은 1번만(블록 스코프)
// const : 할당 및 선언 1번만(블록 스코프)