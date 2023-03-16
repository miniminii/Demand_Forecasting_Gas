# Demand_Forecasting_Gas
[LSTM/XGBosst/Castboost] Dacon 가스공급량 수요예측 모델 개발 대회

<br>

## 💻프로젝트 소개
- **목적:** 시간단위 공급량 데이터 및 기상정보 등 외부데이터를 이용해 일간 공급량을 예측하는 모델 개발
- **참가 대회:** 데이콘 가스공급량 수요예측 모델개발
   - https://dacon.io/competitions/official/235830/overview/description

- **기간:** 2021.09~2021.12
- **팀원:** 12기 전지우, 13기 김현지, 13기 전보민, 14기 김유민, 14기 임혜리  <br>

<br>

## 📑사용 데이터셋
**1. 대회 제공 데이터** : 한국가스공사 시간별 공급량 데이터


**2. 외부 데이터**

- 전산업생산지수
- 가스기름 상대가격
- 가스전기 상대가격
- 2013 ~ 2018년 기온 데이터

> **출처:** 
  - 공공데이터포털(https://www.data.go.kr/index.do), 
  - 기상자료개방포털(https://data.kma.go.kr/cmmn/main.do) 

<br>

## 활동 내용

**1. 데이터 구축**
- 외부 데이터 수집 : 기상 데이터, 경제지수(=전산업생산지수), 가스 대체제 가격(=가스기름 상대가격지수, 가스전기 상대가격지수)
- EDA를 통한 더미변수 생성

**2. 데이터 전처리 및 파생변수 생성**
- 월별, 공급사 구분 별 이상치 처리 : IQR방식
- 추가 변수 추출

**3.모델링 + 하이퍼 파라미터 튜닝**
- XGBoost 단일모델, XGBoost + LGBM 앙상블, ExtraTree Regressor 모델 이용
- 하이퍼파라미터 튜닝 함수 정의
- 최종 대회 30위권 기록

<br>

## 🗓️프로젝트 진행 일정  

|   주차   |   일정   |   내용   |   과제 및 논의   |
|:----------------------------|:----------------------------:|:--------------------:|:-------------------:|
|  1  | 2021.09.26 | OT | 프로젝트 세분화 |
|  2  | 2021.09.27~2021.10.10 | 전력사용량 예측 코드 리뷰 | Analytics 및 알고리즘 모델링 코드 리뷰 |
|  3  | 2021.10.11~2021.10.31 | 가스공급량 데이터 전처리 | 대회 선정 및 EDA 진행, Baseline 모델 구축 |
|  4  | 2021.11.01~2021.11.20 | 가스공급량 데이터 모델링 | Feature Engineering 및 모델링 |
|  5  | 2021.11.21~2021.12.03 | 가스공급량 데이터 모델링 | 모델 앙상블 및 하이퍼파라미터 튜닝 | 
<br>
