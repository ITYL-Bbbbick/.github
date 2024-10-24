# BeBig : 금융 공공데이터 포탈 기반의 고객 금융자산 분석 비교 서비스
link : http://bbbbick.duckdns.org:5173/user

<table>
<tr>
<td style="width: 20%">
<img src="https://github.com/user-attachments/assets/7d6467b1-e49a-4c55-8c2c-b2941bff450c" alt="서비스 스크린샷""/>    
</td>
<td>

### [Front-end]
- Vue.js : 3.5.3
- pinia : 2.2.2
- vite : 5.3.1

### [Back-end]
- SDK : 17 Oracle Open JDK 17p
- Language level : SDK default
- Gradle
  - Distribution : Wrapper
  - Gradle JVM : JAVA_HOME Oracle OpenJDK 17
  - Tomcat : 9.0.91
  - Spring 3
  - Spring Security
      - jwt
  - Spring Batch 4.3.10
      - Quartz 2.3.0
  - SqlSessionFactory

### [데이터베이스]
- mySQL : 8.0.39
- MockData 저장하여 실제 서비스 환경에 가깝게 구현하고자 함
  - 구성한 데이터 현황: 
  - 유저 MockData 약 1만명 / 외 팀원 7인 실제 데이터
  - 계좌 MockData 약 2만5천개 / 실제 계좌 20개
  - 거래내역 MockData 약 9만개 / 실제 계좌별 1년치 거래 내역
</td>
</tr>
</table>

</br>

## 1. 팀 소개
![image](https://github.com/user-attachments/assets/f5ad93fa-fefa-4f0e-b50a-d1beec0d2923)

</br>

## 2. 프로젝트 개요 및 소개

### (1) 💸프로젝트 주제 및 기획 배경
최근 빠르게 변화하는 금융 환경 속에서 개인의 자산 관리와 소비 습관은 경제적 성공을 좌우하는 핵심 요소로 떠오르고 있습니다. 그러나 많은 사람들이 자신의 자산을 효과적으로 분석하거나 목표에 맞는 금융 상품을 찾는데 어려움을 겪고 있으며 특히 소비 습관 개선에 대한 실질적인 도움을 받기 힘든 상황입니다. 이에 따라 금융 공공데이터를 활용해 개인화된 자산 분석과 맞춤형 소비 개선 방안을 제시하는 서비스가 필요합니다. 이러한 서비스를 통해 사용자는 자신의 재무 상태를 명확히 이해하고 목표를 달성할 수 있는 효과적인 방법을 찾을 수 있습니다.

### (2) 프로젝트 추진 배경
![image](https://github.com/user-attachments/assets/226531ed-50d7-4cb6-bbb8-3a043e809d1e)

<br>

최근 서로의 저축/지출 내역을 서로 평가하는 오픈채팅방 '거지방'까지 등장하게 됨
![image](https://github.com/user-attachments/assets/9ac576e7-7f57-4a44-878e-f3df969a9c83)

돈을 모으는데 가장 기본적인 행위인 '저축'에 초점을 맞추어 beBig에서 시키는 대로만 하면 돈을 잘 모을 수 있다는 인식을 심어주자 라는 목표를 갖게 됨

### (3) 서비스 소개
| 사용자의 소비 성향에 맞춘 자산 분석 서비스

### (4) 프로젝트 타겟 - 사용자 페르소나
![image](https://github.com/user-attachments/assets/e96a2c2e-53d9-4f06-aca1-dc1baf8f69ca)


### (5) 프로젝트 목표
⭐️ 사용자의 자산 분석을 통해 개인화 미션과 상품 추천을 제공하여 경제적인 소비 습관을 개선하는 것 ⭐️

① **자산 분석을 통한 소비 습관 개선**

사용자의 자산 상태를 체계적으로 분석하고 이를 바탕으로 최적의 금융 상품 추천 및 소비 습관 개선 방안을 제시합니다.
    
② **소비 습관 개선을 위한 미션 제공**
    
사용자의 소비 패턴을 분석하여 일일 및 월별 맞춤형 미션을 제공합니다.
이 미션을  통해 사용자는 점진적으로 소비 습관을 개선하며 자산을 효과적으로 관리할 수 있게 됩니다.
    
③ **개인 맞춤형 금융 상품 추천**
    
사용자의 금융 유형에 맞춰 금융 공공데이터를 활용하여 최적의 예·적금 상품을 추천합니다.
특히 이자율과 사용자의 주 거래 은행 데이터를 기반으로 개개인에게 맞춤화된 상품을 제공하여 더 나은 금융 의사 결정을 지원합니다.
    
⑤ **정보 공유를 통한  커뮤니티 활성화**
    
사용자 간 자산 관리 및 금융 상품에 대한 정보 공유를 촉진하는 커뮤니티를 제공하여 경제적인 지식을 쌓을 수 있는 상호 학습과 협력을 장려합니다.
다른 사용자의 자산 관리 노하우를 배우고 함께 성장할 수 있는 기회를 제공합니다.

</br>

## 3. 주요 기능 소개

### (1) 로그인
* 일반 / 소셜 / 게스트 로그인

![image](https://github.com/user-attachments/assets/0a7098bf-805e-4b25-8542-c9bc3899a859)


### (2) 계좌 연결
* 페이지네이션과 무한 스크롤을 이용한 거래내역 조회
* CODEF API를 활용한 실제 계좌 연결

![image](https://github.com/user-attachments/assets/9979ef2c-9eda-46bd-b316-e567044d58e9)


### (3) 자산 분석
* 연결된 계좌를 바탕으로 자산을 분석
* **금융 공공데이터 API**를 활용한 예/적금 상품 추천

![image](https://github.com/user-attachments/assets/8da11dc5-c6c4-4f56-a46c-a8beeeaa03b8)


### (4) 유형 검사
* 사용자 페르소나를 기반으로 소비 유형 검사
* 사용자 마다 소비 유형을 가지며, 추후 유형에 따른 미션을 부여받음

![image](https://github.com/user-attachments/assets/43e9882e-ff1b-45e5-96df-17079659abf1)


### (5) 개인화 미션 부여
* 월간 미션 / 일간 미션을 랜덤으로 부여
* 이번달 미션 달성도를 확인할 수 있게함
* 지난달 미션 달성도에 따른 뱃지 부여

![image](https://github.com/user-attachments/assets/70b4eddb-f1d4-41fe-a69b-19ecf75240a0)


### (6) 커뮤니티
* 사용자 간 자산 관리 및 금융 상품에 대한 정보 공유를 촉진하는 커뮤니티를 제공
* 필터링 기능 구현(카테고리, 소비 유형, 좋아요순, 최신순)
* 게시글 페이지네이션 기능 구현
* 사진 최대 3개 업로드 가능

![image](https://github.com/user-attachments/assets/3374f1e0-2e66-4e21-8ab6-8065ff5818e0)

</br>

## 4. 사용도구 및 기술

### (1) 시스템 아키텍처

![image](https://github.com/user-attachments/assets/38a94241-bbb5-4160-a099-39cdce2c6d9c)

### (2) ERD

![image](https://github.com/user-attachments/assets/c6f8eeba-c3fc-4e45-a8ff-9f6d6574acb7)

### (3) Tailwind CSS & 반응형 웹(FE)
- Tailwind 표준 BreakPoint 활용해 반응형 웹 구축
    - 모바일 /PC 버전 모두 제공
- 유틸리티 클래스 사용으로 훨씬 짧아진 코드
    - 평균 150줄의 style 코드 감소
    - 클래스 명명의 번거로움을 덞
- 매우 세밀한 UI 디자인 기능

![image](https://github.com/user-attachments/assets/f660b7d4-fc69-4359-a8a2-a47584d340d8)
![image](https://github.com/user-attachments/assets/d1c82d70-2d93-4c2b-84ea-ac20ed172b18)


### (4) JWT를 통한 로그인 관리(BE)
![image](https://github.com/user-attachments/assets/634286fc-2221-477d-8571-ba59b45f765d)

### (5) OAuth2.0을 통한 소셜 로그인 구현(BE)
![image](https://github.com/user-attachments/assets/7bda8196-6190-48e8-8035-1497580aa186)

### (6) Codef API를 통한 실제 계좌 정보 조회 기능 구현(BE)
![image](https://github.com/user-attachments/assets/e2c769e4-b90c-46cc-890f-cc3cb0a2f1fb)


### (7) Spring Batch와 Quartz를 통한 스케쥴링 및 데이터 처리(BE)
![batch](https://github.com/user-attachments/assets/42632d07-c7a2-4619-87f2-f9927faddb5e)

### (8) GitHub Action을 이용한 CI/CD(BE)
![image](https://github.com/user-attachments/assets/ac82ad49-18d8-4823-a3b8-e214eeb184f1)


### (9) 배포
- AWS : ec2, S3
  
</br>

## 5. 사용 협업 툴
**- Jira, Notion, Github, Figma**

### (1) Jira
- Jira를 사용해 WBS를 만들어 일정, 진행상황, 담당자 파악을 정확히 함
- 자동화를 이용해 이슈를 빠르게 파악하고, 현재 진행 상황과 담당자와의 소통 향상
![image](https://github.com/user-attachments/assets/913e3887-e945-486f-bfd2-e999afc1f84f)
![image](https://github.com/user-attachments/assets/7462f602-a0fa-4d3f-9038-bf1c7d4d22bc)

### (2) Notion
![image](https://github.com/user-attachments/assets/729477b6-5604-4d4d-8137-5f3ca4636e40)

### (3) Github
**Git flow**
![image](https://github.com/user-attachments/assets/bc9a2365-0193-4b79-9420-ea329666b82a)

**Git Convention 정의**
![image](https://github.com/user-attachments/assets/57f1d7a8-3b65-4ae9-b416-525f6a87397d)

**PR 리뷰**
![image](https://github.com/user-attachments/assets/10bcb995-1168-487f-ac3e-9258db3c5a00)

### (4) Figma
![image](https://github.com/user-attachments/assets/4968aebe-1cca-4618-b7c4-b95d884bc9b4)


