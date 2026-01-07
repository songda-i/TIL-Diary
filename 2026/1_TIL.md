# 1_TIL_Private

:purple_heart: Java

:green_heart: 인프라 - AWS

:handshake: PJT업무

:crescent_moon: 달이 조언​

:heart: 개념/용어

:blue_heart: 글/영상

:books: 책/강의

---
:green_heart: AWS

1.인강 : AWS 강의실

---

## 1/1(목)
:green_heart: AWS

## 1/2(금)
:green_heart: AWS

## 1/3(토)
:green_heart: AWS
- S3 
    - 스토리지 클래스
    - 버전관리
    - 수명주기

:heart: OTel

- OpenTelemetry (OTel) : 오픈 소스 통합 가시성 프레임워크
    - 클라우드 네이티브 컴퓨팅 재단(CNCF)에서 텔레메트리 데이터를 수집하고 통합 가시성 백엔드로 전송하는 방식을 표준화하기 위해 개발
        - 이전에 쓰던 OpenTracing과 OpenCensus 을 단일 프로젝트로 합친 것
            - OpenTracing: 특정 벤더에 구애받지 않는 텔레메트리 데이터 전송용 API
            - OpenCensus: 메트릭/추적 수집을 위한 언어별 라이브러리

    - 텔레메트리 데이터(로그, 메트릭, 추적)를 하나의 통합된 형식으로 수집하고 처리하며 내보낸다.
        - 로그: 특정 시점에 발생한 개별 이벤트의 텍스트 기록
            - 예시: 타임스탬프, 사용자 ID, IP 주소가 기록된 로그인 시도
            - 적합한 용도: 문제 해결, 디버깅 및 코드 실행 검증
        - 메트릭: 시스템 성능을 반영하는 시간 경과에 따른 수치 측정값(시계열 데이터)
            - 예시: CPU 사용률 70% 또는 HTTP 요청률 1,000/s
            - 적합한 용도: 실시간 모니터링, 알림, 트렌드 분석
        - 추적: 여러 시스템 구성 요소를 통과하는 요청 또는 트랜잭션의 경로로, 스팬으로 나뉜다.
            - 예시: 전자상거래 플랫폼의 마이크로서비스에서 결제 프로세스 추적하기
            - 최적 대상: 분산 아키텍처에서 성능 병목 현상 파악 및 요청 흐름 이해

## 1/4(일)
:green_heart: AWS
- S3

## 1/5(월)
:green_heart: AWS
- RDS

## 1/6(화)
:green_heart: AWS
- RDS

## 1/7(수)
:green_heart: AWS
- RDS