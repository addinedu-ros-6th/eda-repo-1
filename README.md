# 의료 로봇 섹터 뉴스 데이터 감성 분석을 통한 주식 시장 경향 분석

> ***과연 뉴스 데이터의 긍정-부정 수치를 보고 주식 매도-매수를 해도 될까?*** <br>
> ***뉴스 데이터와 주식 시장 경향에 유의미한 연관성이 있을까?***
<br />

## 🤖 프로젝트 소개
- 본 프로젝트는 뉴스 기사의 정서와 그것이 주가에 미치는 영향을 분석함으로써 시장 행동과 일반적인 투자 전략의 타당성에 대한 더 깊은 이해를 제공하는 것을 목표
<br />

## 🧠 구성원 및 역할
|이름|업무|
|:---|:---|
|고선민|- 미국 섹터 Google 웹크롤링 및 전처리 <br> - pipeline을 통한 미국기사 감성분석 <br> - plotly를 통한 주식과 뉴스 데이터의 감성분석 상관관계 및 키워드 시각화|
|강지훈|- 한국 섹터 Naver 웹크롤링 및 데이터 전처리 <br> - yfinance를 통한 기업별 평균 종가 데이터 시각화  <br> - 뉴스 기사량과 주식의 상관관계 분석|
|김주영|- 한국 섹터 Naver 웹크롤링 <br> - 주식 시작 경향 파악 및 데이터 수집 <br> - 종목별 특정 구간에서의 이동평균선 특이점 분석 및 시각화|
|이세형|- Roberta DL 모델을 활용한 자연어 학습 및 감성분석 <br> - DB 구축, 관리, 및 Query 작성 <br> - 뉴스데이터와 주식의 등락에 대한 상관관계 분석|
<br />

## 🖥️ 활용 기술
|구분|상세|
|:---|:---|
|개발환경|<img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white" /> |
|IDE| <img src="https://img.shields.io/badge/VSCode-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white" /> <img src="https://img.shields.io/badge/Jupyter-F37626.svg?&style=for-the-badge&logo=Jupyter&logoColor=white" /> <img src="https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252" />|
|언어| <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />   |
|EDA 시각화|<img src="https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white" /> <img src="https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white" /> <img src="https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white" /> <img src="https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black" /> <img src="https://github.com/user-attachments/assets/e6aabca4-a5da-43ed-ba67-fa243e54ff74" />|
|웹 크롤링| <img src="https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=Selenium&logoColor=white" /> Newspaper3k| 
|DB|<img src="https://img.shields.io/badge/Amazon_RDS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white" /> <img src="https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white" />|
|협업|<img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" /> <img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white" /> <img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white" /> |
<br />

## 📜 웹 크롤링 및 데이터 전처리 과정

### 기업 및 사이트 선정
- 한국 및 미국 기업들은 코스피, 나스닥/뉴욕증권거래소에 등재된 의료 로봇 섹터를 기준으로 선정.
- 한국 기사들은 네이버 기사, 미국 기사들은 구글 뉴스를 통해 크롤링 진행.

### 크롤링 데이터 수집 (네이버 한국기사)
- 크롤링 데이터 : **"date", "title", "content", "link"**
- 검색어: "surgical robot OR medical robot", "Intuitive+Surgical", "Stryker+Corporation", "Medtronic", "Globus+Medical", "Asensus+Surgical", "Smith+%26+Nephew", "Johnson+%26+Johnson"

### 크롤링 데이터 수집 (구글 미국기사)
- 크롤링 데이터 : **"date", "title", "content", "link", keyword"**
- 검색어 : "의료 로봇", "고영", "큐렉소", "미래컴퍼니"

### 수집 데이터 전처리 (네이버 한국기사)
- 크롤링 과정에서 잘못 가져와진 데이터들과 date가 nat 값인 데이터들을 제거 

### 수집 데이터 전처리 (구글 미국기사)
- 내용내용내용

<br />

## 🧑‍💻 감성분석
### 감성분석 모델 적용 (pipeline)
- 내용내용내용

### Roberta 딥러닝
- RoBERTa는 BERT의 개선 버전으로, 더 많은 데이터와 긴 훈련 시간, 동적 마스킹, 그리고 다양한 최적화 기법을 통해 NLP 작업에서 뛰어난 성능을 보인다는 자료가 있어 학습모델로 선정하였다.<br>
  주요 개선점으로는 더 큰 데이터셋 사용, 동적 마스킹, 그리고 문장 순서 예측 제거 등이 있다.<br><br>
- 기존의 감정분석 모델과 수집한 뉴스데이터로 파인튜닝한 Roberta 모델의 뉴스데이터와 주식의 등락에 대한 상관관계 예측율 비교

| 기존 사용 모델 | Roberta 딥러닝 추가학습 시킨 모델 |
|:--------------:|:----------------------------:|
| ![original_model_senti_result](https://github.com/user-attachments/assets/b38b76d9-8004-44aa-9f6b-7bda3c86b52f) | ![model_fine-tuned_with_roberta_result](https://github.com/user-attachments/assets/92857fe1-1ffd-4798-9aa8-4c9630e45c42) |
<br />

## 🗂️ 데이터 베이스 구축
### 테이블 목록

- article(기사테이블)
- stock_info(주식정보 테이블)
- sentiment(감정분석 테이블)
- keyword(키워드 테이블)

### TABLE ERD
![database_tabel_erd](https://github.com/user-attachments/assets/7f8041b3-6cbd-44f2-8e0b-fee195db47d0)
<br /><br />

## 🗂️ 데이터 분석 및 시각화
### 뉴스 기사량과 주식의 상관관계
![image](https://github.com/user-attachments/assets/c4d40715-360e-4559-b65d-b217bd79b292)
- 기사량과 주식의 등락을 비교해보고 분석하려 했으나 데이터 전처리 과정에서 누락된 기사량이 많아서 기사량만으로는 분석할수없음을 인지

### 뉴스 데이터와 주식의 등락에 대한 상관관계 분석
- (대표 시각화 자료 한두개)
- (설명 한줄)

### 주식과 뉴스 데이터의 감성분석 상관관계 및 키워드 시각화
- (대표 시각화 자료 한두개)
- (설명 한줄)

### 특정구간에서의 특이점 파악
- 특정 구간 산출
    - 상위 5%의 기울기를 갖는 구간 + 상위 5%의 기울기를 갖는 구간 중 상위10% 밀집 구간 + MA10과 MA20 골든크로스
    - ![0304_Top3_period](https://github.com/user-attachments/assets/65db3321-4e69-4197-8545-7d664e0924eb)
- 거래량 200%이상 밀집 구간에서의 관련 기사 본문의 감성 분석 차트
    - ![05_volumeKDE_sentiment](https://github.com/user-attachments/assets/fd1b2a23-7ba5-47f8-85dd-e74a83eb1b0c)
- 세 개의 분석 지표를 통해, 특정한 기간(분석하고자하는 기간)을 산정하고, 두 개 이상의 지표가 겹치는 구간 중에서 기간 내 상승률이 가장 높은 구간 세 곳을 특정함
  - 특정된 세 개의 구간들에서 유의미하다고 볼 수 있는 부분을 발견 할 수 있었음
    - 종가선이 20MA를 올라타기 직전의 차트 모습과 유의미한 대량의 거래량이 터지기 직전의 구간을 특정한 것을 확인 할 수 있었음
- 거래량 200% 이상 구간에서의 관련 기사 본문 감정 분석
  - 긍정과 부정 중, 비율상으로는 긍정적인 감정의 기사의 양이 약 1.8배가량 많았음
- 소결

<br />


## 💭 결론
- 뉴스 데이터로 주식 시장 경향을 완전히 분석하기엔 한계가 존재함.
- 하지만, 뉴스 키워드와 감성 분석 결과는 보조 지표로서의 충분한 역할을 함.

