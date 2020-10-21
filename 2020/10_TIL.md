# 10_TIL_Diary

:apple: 진짜 긍정은 내 삶에서 내가 할 수 있는 일을 하는 것

:black_heart: Java

	-  난 정말 자바를 공부한 적이 없어요(윤성우)

:green_heart: Python

:handshake: PJT

:heart: 개념/용어

:blue_heart: 글/영상



## 10/05(월)

### :blue_heart: GPT-3 (Generation Pre-trained Transformer 3)

* 딥러닝을 이용해 인간다운 텍스트를 만드는 자기회귀언어모델
  * 개발사 : OpenAI(feat. 일론머스크) 대표 : Sam Altman
  * 2020.06.11 베타출시, 2020.09.22 마이크로소프트 독점계약
  * 가능영역 : 칼럼작성,자유대화, 번역, 디자인, 코딩 ...

## 10/20(화)

- :blue_heart: 프로젝트에 필요한 기술 스택이라면 사용하기 

  - 최신 기술이라서 아니고 사용해야 하는 이유가 있을 때
  - 성능,보안, 대용량 구조 등 이유가 있을 때
  - 사용했다면 기본적인 것들 대답준비, 자기소개서랑 포트폴리오에 키워드 포함


## 10/21(수)

### :blue_heart: 데이터 크롤링 / 스크래핑

- 인터넷에서 데이터 수집하는 방법
  - 1 사람이 수작업으로 데이터 수집
  - 2 OpenAPI 공개된 데이터 얻는 방법
  - 3 HTTP Get Method 사용해 HTML 가져오는 방법
  - 4 Selenium Web Driver 사용해 사람이 하는 것과 유사한 자동화 방법 : (웹사이트 테스트 자동화 목적으로 개발)

- 크롤러(크롤링)와 스크래퍼(스크래핑) 구분하기!

  - :arrow_forward: 스크래퍼 : 웹사이트에서 정보를 추출하는 프로그램
    - 상품별 가격 알기 위해 해당 상품 파는 페이지들의 가격 추출
  - 크롤러 : 조직적,자동화 방법으로 웹 탐색/수집하는 프로그램
    - 구글, 네이버 등 검색 엔진 결과 데이터 수집하는 봇(Bot)

- **robots.txt** 검색 로봇

  - 웹사이트주소/robots.txt

    - www.google.com/robots.txt
    - www.daum.net/robots.txt

  - robots.txt 보고 서버의 로봇 배제 표준 준수 할 것

  - ```
    모든 검색엔진이 긁어가는 것 모두 막기
    User-agent: *
    Disallow: /
    ```

  - ```
    모두 허용
    User-agent: *
    Disallow:
    ```

