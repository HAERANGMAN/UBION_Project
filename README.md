# UBION_Project

금융빅데이터 분석을 위해서는 기술적으로 단순히 접근하는 것이 아니라 기획자로서 노력해야 한다.   기술적인 부분도 물론 중요하지만, 데이터 사이언티스트의 역량을 잘 발휘하려면 목적성에 맞는 분석을 해야한다.   따라서 내가 원하는 정보를 얻기 위해서 도메인 지식을 활용하고 방향성을 명확히 잡아서 접근해야 한다.   또한, 통계지식을 활용한 결과치 해석을 절대로 놓치면 안된다.


**기업 부실 분류**
-	부실기업에 대한 논의도 필요함. (어떤 것을 부도로 설정할 것인지)
- 상장폐지, 채무 불이행, 오너리스크, 분식회계 등 다양한 요소가 존재하는데 부실에 대한 정의를 정확히 하고 넘어가야 함. 
- 지금까지 결측치 전처리를 시행했으나, 이젠 정의와 방향성에 맞는 전처리를 시작해야 한다.
- 참고로 자산가치보다 부채가치가 높은 경우, 부도로 보는 [블랙-숄즈 모형](https://ko.wikipedia.org/wiki/블랙-숄즈_모형)도 존재한다.

프로젝트 스케줄 관리
-	프로젝트가 어느정도 진행됬지만, 아직도 데이터를 찾고 있다면 이는 데이터 분석가의 능력 부족으로 판단된다.


## 프로젝트 일정

데이터 사이언티스트 역량을 높이기 위한 것으로 일정은 다음과 같습니다.

![image](https://user-images.githubusercontent.com/87803612/141708330-942e987e-48d3-4133-9c35-69fdcb86e3b3.png)

먼저 첫주차 금요일에 관심 논문 발표를 할 예정입니다.
프로젝트 계획서 발표는 화요일, 목요일 중 선택할 예정이고 추후에 업로드하도록 하겠습니다.


## 주의할 점

데이터 분석 목적 정의 
- 데이터 탐색한 결과를 작성해야 합니다. [관련 디렉토리 : Diary 폴더](https://github.com/signature95/UBION_Project/tree/main/Diary)
- 데이터 분석 추진 배경 및 목적을 기술합니다. [관련 디렉토리 : Paper 폴더](https://github.com/signature95/UBION_Project/tree/main/Paper)
- 데이터의 출처를 작성합니다. [관련 디렉토리 : Dataset 폴더](https://github.com/signature95/UBION_Project/tree/main/Dataset)
- 분석 기법을 작성합니다. [관련 디렉토리 : Study 폴더](https://github.com/signature95/UBION_Project/tree/main/Study)
- 최종 보고서를 작성합니다. [관련 디렉토리 : Report 폴더](https://github.com/signature95/UBION_Project/tree/main/Report)

데이터 분석 과정 정리
- 프로젝트의 진행 과정을 도식화, 시각화해서 정리합니다. (물론 word 파일로 해도 되지만, 되도록 시각화하여 이해도를 높이려합니다.)

## 데이터 분석 모델 정의서 예시

<img width="1014" alt="스크린샷 2021-11-15 오전 10 33 30" src="https://user-images.githubusercontent.com/87803612/141708796-5912d082-8260-4f34-ac89-453990b4fe0e.png">

## 빅데이터 비지니스의 핵심 성공 요인
- 빅데이터 분석 목적, 사용자, 활용 목적에 대하여 명확하게 정의한다.
- 데이터 볼륨보다는 가치 창출 관점에서의 검토가 필요하다
- 업무 전문가의 참여가 필수적이다 (협업의 필요성)
- 분석 목적에 따라 분석 모델을 정의한 후 분석 인프라 요건을 검토한다
- 지속적으로 분석 모델 개발, 분석 시스템 구축 후 주기적인 모델 유의변수를 모니터링하고 정제한다
- Start Small: 작은 규모로 시작하고, 성공 사례를 공유하고 확장하는 형태로 추진한다

## 도메인 지식
- 은행의 영업점에서는 보통 기업 규모의 대출을 진행하고 있지 않습니다. (접수만 진행함)

<img width="913" alt="스크린샷 2021-11-15 오전 11 02 57" src="https://user-images.githubusercontent.com/87803612/141710917-93ca23e9-b4be-44c0-b706-f5982558e94d.png">


### 기업의 자금 대출 종류
- 자금시설자금(부동산, 기계장치 등 기업 시설에 투자하는 자금으로 보통 만기 10년으로 가져감)
- 운영자금(1년 단위로 기업의 운영을 위해 필요한 자금)
- 따라서 연체 예측이 중요함
1. 이자납부 기간 + 분활상환기간
2. 공장을 짓는 기간동안에는 이자만 납부하게됨. 기업의 입장에서는 자금시설자금 대출이 더 부담스러움.
3. 따라서 기업의 매출 규모를 보고 은행이 대출을 결정하게 된다.
4. 참고로 10억이상의 대출 규모가 있는 경우, 외부의 신용정보회사가 평가하게 되는데 이번 자료에서는 대부분 10억이상의 여신을 보유한 회사가 데이터에 있을 것임.

#### 참고
- 신용등급과 부도율은 어느정도 상관관계가 존재한다.
- 무담보기업어음을 발행하는 기업은 반드시 외부 신용조사를 받게 되있다.
- ABS(자산유동화증권)을 발행하는 경우도 신용조사는 의무적이다.
- 기업의 담보는 부동산원(과거 한국감정원)이 보통 기업이 소유한 부동산을 평가하게 된다.
- 여신기획부서
  -  은행의 여신기획부서는 중소기업, 대기업 대출 규모를 적절하게 조절한다. (물론 중소기업에 전문적으로 대출을 실시하는 IBK중소기업은행이 존재한다)
  -  사후관리부서는 여신을 제공한 후 기업의 부실여부를 모니터링하개 된다.
  -  이렇게 기획과 사후관리를 나누는 이유는 과거 닉리슨의 베어링 은행 사건이 대표적인 원인이다. 이를 운영리스크 [Operating Risk](https://www.bok.or.kr/portal/main/contents.do?menuNo=200810) 라고 한다

- **중요**
  - 부실기업과 정상기업의 비율이 1:10 정도보다 더 차이가 나는 경우가 대부분이다.
  - 이때, 90개의 정상기업과 10개의 비정상기업이 있다고 가정하고 100개를 전부 정상으로 판별하는 경우, 정확도는 0.9에 육박하는 오류가 발생한다.
  - 따라서 bias(편향성)을 조절하여 정확도를 과대평가하는 경우를 가정해야 하므로, 주의해야 한다,
  - 이때 **균등랜덤**이라는 개념이 들어간다.
<img width="1039" alt="스크린샷 2021-11-15 오후 1 46 08" src="https://user-images.githubusercontent.com/87803612/141723985-8ba306f4-8411-45ed-b451-21a8ceb7ea0e.png">

  - 기업의 **재무 지표**는 다음과 같다.
<img width="918" alt="스크린샷 2021-11-15 오후 1 51 35" src="https://user-images.githubusercontent.com/87803612/141724513-3197ee35-4aa3-46b1-8c88-ab2b31bcb71c.png">

  - 비재무 지표도 참고할만 하다. (CEO와 기업의 직종이 동일한지 여부를 더미변수로 설정해도 됨. 이런 형태로 비재무지표를 더미로 넣고 분석해도 된다)
  - 경기 순환에 대한 것도 참고해야 함. (경기 둔감업종, 민감업종 등을 구분해서 사용해야 함)
  - 기업의 위험
    - 경영 위험, 재무 위험, 영업 위험, 산업 위험

## 발표 형식
1. 논문선정
- List 내에서 선택 또는 자유 선정
2. 발표 방법 및 발표자료 : 자유
3. 발표형식
- 팀 소개
- 논문 선정 이유
- 데이터 수집, 기간 등
- 데이터 전처리 과정
- 관련 선행연구
- 분석전 탐색과정(기초통계량, 상관계수 등)
- 분석방법(다수방법 비교의 경우 소개)
- 실증결과 및 검증 ( 분석방법에 따른 검증평가)
- 기대효과
- 한계점

## 참고 사이트
- [kis Value](https://www.kisvalue.com/web/index.jsp)
- [재무비율정보](https://comp.fnguide.com/SVO2/ASP/SVD_Main.asp?pGB=1&gicode=A034950&cID=&MenuYn=Y&ReportGB=D&NewMenuID=Y&stkGb=701)
  - 컨센선스 스크리밍이 가장 중요하긴하지만, 이번 프로젝트에선 필요하지 않을 수도 있음.
  - 여기 사이트에는 기업 정보를 전부 확인이 가능한 부분에서 유용함.
- [전자공시DART를 활용한 재무비율일괄다운](https://opendart.fss.or.kr/disclosureinfo/fnltt/dwld/main.do)
  - 일반적으로 알려진 PER, EPS 등에 대한 정보만 확인가능함. 제한적으로 알 수 있는 점이 아쉬움.
- [TS2000](http://www.kocoinfo.com)
  - 주가, 재무비율 등 다양한 정보를 얻을 수 있고 데이터 기간도 길게 잡을 수 있다.
 

## 역할
논문발표 : 이주희
중간발표 : 신문혁
최종발표 : 정기호
Q&A : 윤영주 + 나머진 support
질문자 : 다 같이 진행


## Contributors
- [정기호](https://github.com/signature95)
- [이주희](https://github.com/fredlee613)
- [신문혁](https://github.com/MarvinShin)
- [윤영주](https://github.com/younyoungju)

## 조이름
- Trillion (1조)
