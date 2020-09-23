# 9_TIL_Diary

:apple: 진짜 긍정은 내 삶에서 내가 할 수 있는 일을 하는 것

:black_heart: Java https://opentutorials.org/course/1223 (2013년도 제작, 2020년도 리뉴얼)

:green_heart: Python

:handshake: PJT

:heart: 개념/용어

:blue_heart: 글/영상



## 09/01(화) - java

* :black_heart: 생활코딩 java https://opentutorials.org/course/1223/5261
  
  * 유효범위  : 인텔리제이를 통한 실습
  
* :handshake::green_heart: Python  Pandas DataFrame [공식문서](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.head.html)

* ```python
  import pandas as pd
  ```

   `Pandas` 를 이용하여 가공하거나 분석을 한 데이터를 저장 가능

  (사용목적에 따라 5가지 저장 방법) [참고](https://tariat.tistory.com/583)

  - ① csv 파일 저장 :ballot_box_with_check:

  - ② 엑셀파일 저장

  - ③ pickle 피클 저장

  - ④  splite3 db 저장

  - ⑤ html 저장

* :blue_heart: ​[글] 댄 아브라모프 -리액트개발자 : 2018년 내가 모르는 기술들  https://overreacted.io/ko/things-i-dont-know-as-of-2018/

  ```
  [면접TIP]  내가 생각하는 완벽한 이상 때문에 좀만 머릿속에서 꼬이면 아예 말을 못하는 사람들... 기술 면접에 주어야 하는 인상 :  차분히 충분히 생각해서 논리적으로 정리해서 말하자.  알음알음 하겠다. 써보지 않았지만 이 개념은 알고 있다.
  ```



## 09/05(토) - SQLD

> 08/24 ~ 09/05 2주간 SQLD 자격증 준비 및 시험
>
> - 교재 : SQL자격검정실전문제(한국데이터산업진흥원,2020) , SQL개발자기출문제(이기적,2020)

- :heart: 배우게 된 것

  - 트랜잭션(ACID, (원자성, 고립, 지속갱신, 일관전후))

  - 속성과 엔티티, 메인쿼리와 서브쿼리

  - INNER / OUTER JOIN (FULL / LEFT / RIGHT)

  - SQL server / oracle 문법 차이

  - ROLLUP / CUBE / GROUPING SETS

  - RANK / DENSE_RANK / ROW_NUMBER

  - NVL / NULLIF / COALESCE

    


## 09/06(일) 

- :black_heart: 생활코딩 java
  - 유효범위



## 09/07(월) 

- :black_heart: 생활코딩 java
  - 초기화와 생성자
- :handshake: :heart: 깃브랜치 :  https://backlog.com/git-tutorial/kr/stepup/stepup1_1.html
- :green_apple: 일정관리 핵심은 **각 업무의 분리**와 **병렬적 진행** !



## 09/08(화) 

- :black_heart: 생활코딩 java
  - 상속과 생성자 : 
    - 상속(Inheritance)이란 물려준다
    - 상속의 필요성 : 기존의 객체를 그대로 유지하면서 어떤 기능을 추가하는 용도
    - 부모/자식, 상위/하위, super/sub, 기초/유도, base/derived 클래스
  - 오버로딩 : 같은 이름의 메서드명과 다른 갯수의 매개변수인 메소드들을 여러개 만들기
  - 오버라이딩 : 부모클래스의 메소드를 자식클래스에서 가져와 다르게 동작하게 하기
- :blue_heart:  백엔드 개발자를 꿈꾸는 학생에게 https://d2.naver.com/news/3435170
  - 체득의 영역, 신입개발자의 목표로 잡을 수준
    - 개발도구의 공식 레퍼런스를 보고 사용법을 스스로 익힐 수 있음
    - 자신이 경험한 사용법을 문서화해서 팀 내에 전파할 수 있음
- :blue_heart: REST API 룰 : https://docs.microsoft.com/ko-kr/azure/architecture/best-practices/api-design
  - api-design 의 Naming Rule 명명 규칙은 매우 중요

- [면접대응] Vue 손쉽게 하므로 효율적으로 빠르게 할 수 있었다. 원론인 자바스크립트의 소중함을 알고 더 공부하고 있다. 



## 09/09(수)

- :black_heart: 생활코딩 java
  - 클래스 패스
- :blue_heart: AWS : 아마존 웹 서비스는 아마존닷컴의 클라우드 컴퓨팅 사업부. 아마존 웹 서비스는 다른 웹 사이트나 클라이언트측 응용 프로그램에 대해 온라인 서비스를 제공
  - AWS 머신 스펙은 개발 노트북 장비 비슷
  - 고정된 트랜잭션에겐 고비용
  - 중요한 리소스가 물리적으로 내가 제어 할 수 없는 공간이 있다
  - :handshake: 이번 주 할 일 : 개발환경을 AWS VM 에 올려보기.
    - VM 은 텅빈 사무실 공간, 설비가 없음
    - 서비스에 필요한 DB, Web Server, WAS 설치 필요
    - 소스 저장소(Gitlab)로부터 자동화된 어플리케이션 배포가 최종 목표(잰킨스)

- :blue_heart: HTTPS
  -  암호화의 핵심은 갈취당하더라도 사용할 수 없도록 만드는 것.
  - 현실적으로, http 요청이 네트워크를 타고 패킷이 전송되는 것이지만, 그걸 참 잘 훔쳐가더라.
  - 법적으로 일정 규모 이상 서비스는, HTTPS 의무
  - 관련용어 : 네트워크, 패킷, 스누핑
- 웹서버 
  - Web Server : 정적, 기성품전달하기
  - Web Application Server : 동적, 제조해서전달하기
- Fiddler(피들러), Wireshark : http 네트워크 요청 내용을 모니터링 할 수 있다. (네트워크 패킷 모니터링)
- Postman : 클라이언트에서 http 요청을 쉽게 생성하여 보낼 수 있다.



## 09/10(목)

- :black_heart: 생활코딩 java
  - 패키지

## 09/11(금)

- :black_heart: 생활코딩 java

  - API 

  - 규제 : 추상 클래스, final, 접근 제어자, 인터페이스 

  - 접근제어자

  - :one: 클래스의 맴버(변수와 메소드)들의 접근 제어자 : public, protected, default, private 

    - |                             | public | protected | default    | private  |
      | --------------------------- | ------ | --------- | ---------- | -------- |
      | 같은 패키지, 같은 클래스    | 허용   | 허용      | 허용       | 허용 O   |
      | 같은 패키지, 상속 관계      | 허용   | 허용      | 허용       | **불용** |
      | 같은 패키지, 상속 관계 아님 | 허용   | 허용 O    | 허용 O     | **불용** |
      | 다른 패키지, 상속 관계      | 허용   | 허용 O    | **불용** X | **불용** |
      | 다른 패키지, 상속 관계 아님 | 허용   | **불용**  | **불용**   | **불용** |

  - :two: 클래스의 접근 제어자 : public과 default

    - public class 클래스명 {} 

      - 제약사항) 소스코드의 파일명과 퍼블릭클래스명은 동일,1개만 사용

    - class 클래스명 {}

      - 같은 패키지 내에서만 사용 가능 / 다른 패키지에서는 못 씀

        ```java
        package org...다른패키지;
        import org...있던같은패키지.*;
        
        public class 다른패키지의어느소스코드의퍼블릭클래스명 {
            //Defaultclass defaultclass = new Defaultclass(); //에러
        }
        ```

        

- 체득의 영역

- OSI 7 계층 - 물 데 네 트 세 표 응

## 09/12(월)

- :green_heart: ㅋㅋㅇ 문제풀이 python3

## 09/13(일)

- :green_heart: ㄹㅇ 문제풀이 python3
- :green_heart: 다음웹툰/네이버웹툰/카카오웹툰 python 크롤링

## 09/14(월)

- :heart: REST ​

- REST는 웹의 장점을 최대한으로 활용할 수 있는 네트워크 기반의 아키텍쳐

- RESTful하게 개발을 하면 쉽고, 기존 웹(HTTP)을 그대로 따라가면서도 의미적으로 구조가 잘 잡힌 URI를 만들 수 있음

  - RESTful URI로 URI를 통해 자원(resource)가 /게시판들 중 첫번째 게시판의 글들 중 406번째 글임을 쉽게 알 수 있다.

  ```
  http://class.net/boards/1/posts/406
  ```

- **URI**를 이용해 명시된 자원(resource)에 접근하고,
  자원(resource)에 어떠한 조작(CRUD)을 할 지 **HTTP 메서드**로 나타내는 방법

| HTTP Method | CRUD   | 기능 |
| ----------- | ------ | ---- |
| POST        | CREATE | 생성 |
| GET         | READ   | 조회 |
| PUT         | UPDATE | 갱신 |
| DELETE      | DELETE | 삭제 |



- :handshake::green_heart: **빅데이터 추천 알고리즘**
  
- 빅데이터 추천 알고리즘 방법/시스템 :협업필터링, 컨텐츠기반필터링, 앙상블 기법, 유사도 등...

  - 협업필터링 CF, Collaborative Filtering : 너무나 비슷한 너와 나, 내가 좋아하는 이건 넌 어때?
  - 컨텐츠기반필터링 CB, Contents Based Filtering : 무언가를 좋아한다면, 혹시 이것도 좋아해? 
  - 앙상블 : 
  - 유사도 계산 : 코사인Cosine유사도, 피어슨Pearson, 내적Inner Product, 유클리디안Euclideam거리함수 (협업, 컨텐츠 무시가능)

- Python 추천 시스템 특화 라이브러리  : LigthFM, Surprise, PySpark

  - LigthFM : 기본 및 하이브리드 추천, 데이터가 충분하지 않아도 추천 

    - [공식문서](https://making.lyst.com/lightfm/docs/index.html)

  - Surprise : 협업필터링 위한 알고리즘 제공 라이브러리

    - [공식홈페이지](http://surpriselib.com/)

      ```
      $ pip install numpy
      $ pip install scikit-surprise
      ```

    - [공식문서](https://surprise.readthedocs.io/en/stable/) -함수사용법

    - [튜토리얼](https://blog.cambridgespark.com/tutorial-practical-introduction-to-recommender-systems-dbe22848392b) -numpy 와 surprise 사용 추천시스템 구현

  - PySpark : 대용량 처리 속도 면 이점, 스타크는 분산 클러스터 용도, 머신러닝 알고리즘 포함

    - [공식문서](http://spark.apache.org/docs/latest/api/python/pyspark.mllib.html#module-pyspark.mllib.recommendation)



## 09/19(토)

- :black_heart: 생활코딩 java

  - 예외처리



## 09/20(일)

- :black_heart: 생활코딩 java

  - Object 클래스
    - 모든 클래스가 공통으로 포함하고 있어야 하는 기능을 제공하기 위해서
    - 모든 클래스는 `class O extends Object {}` Object를 상속받고 있음
    - Object 클래스의 메소드
      - toString() : 객체를 문자화시킴
      - equals() :  다형성, @Override, hashCode(), ???
      - finalize() : 객체가 소멸될 때 호출되기로 약속된 메소드, 사용은 비추,자제바람
      - 가비지컬렉션(Garbage Collection, 이하 GC)
      - clone() : 복제

- 상수와 enum(자바1.5부터)

  - interface : 인터페이스에서 선언된 변수는 무조건 public static final의 속성을 갖는다

  - class :  `==`다른 카테고리 상수 비교 금지, switch 문 못씀 

    - ```java
      public static final Fruit APPLE  = new Fruit();
      ```

  - enum : 열거형

    - 생성자의 접근 제어자가 private이다. 그것이 클래스 Fruit를 인스턴스로 만들 수 없다는 것 ???
    - 클래스와 이름이 같은 메소드는 생성자



## 09/21(월)

- :black_heart: 생활코딩 java 2회차 복습
  - 숫자,문자, 변수, 주석, 세미콜론, 데이터타입, 형변환, 연산자, 비교, 불린, 조건문, 논리연산자, 반복문
  - 배열, 메소드, 입출력

- :green_heart: Jump to Python 2회차 복습
  - 자료형 : 숫자형 ,문자열 자료형, 리스트 자료형



## 09/22(화)

- :black_heart: 생활코딩 java 2회차 복습
  - 객체지향프로그래밍, 클래스, 인스턴스, 객체, 맴버, 유효범위
  - 초기화와 생성자, 상속



