## 2. 시스템 구성도

### 2.1 전체 아키텍처

감정 일기장 분석기는 다음과 같은 4개의 주요 구성 요소로 이루어져 있습니다:

![image](https://drop.nodove.com/-3nh5K7FiDk/pasted-2025-04-09T081848.285Z.png)

[mermaid_code](https://drop.nodove.com/-Va3tpGTtL2/pasted-2025-04-09T081927.123Z.txt)



### 2.2 컴포넌트별 역할

#### 2.2.1 Frontend (사용자 인터페이스)

- 사용자 등록 및 로그인 인터페이스
- 일기 작성 및 조회 화면
- 감정 분석 결과 시각화 대시보드
- 추천 컨텐츠 및 알림 표시


#### 2.2.2 Backend (서버 및 비즈니스 로직)

- 사용자 인증 및 권한 관리
- API 엔드포인트 제공
- 데이터 처리 및 비즈니스 로직 수행
- AI 모듈과의 통신 및 결과 처리


#### 2.2.3 AI Module (감정 분석 엔진)

- 텍스트 전처리 및 감정 분석
- ChatGPT API 연동
- 감정 패턴 인식 알고리즘
- 맞춤형 추천 생성

#### 2.2.3-1 AI Module (인지 행동 치료)
- 부정적 감정일 시에만 작동하는 모듈
- 인지 행동 프롬프트


#### 2.2.4 Database (데이터 저장소)

- 사용자 정보 저장
- 일기 데이터 관리
- 감정 분석 결과 저장
- 추천 및 피드백 데이터 관리
- API 사용 시 기존 정보 사라짐 (캐싱 전략 사용)
  
![데이터 캐싱](https://drop.nodove.com/-YmMsjm5Tww/pasted-2025-04-09T083744.441Z.png)

