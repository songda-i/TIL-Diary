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

