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
- 내용내용내용

### 수집 데이터 전처리 (구글 미국기사)
- 내용내용내용

<br />

## 🧑‍💻 감성분석
### 감성분석 모델 적용 (pipeline)
- 내용내용내용

### Roberta 딥러닝
- 내용내용내용
<br />

## 🗂️ 데이터 베이스 구축
- 내용내용내용
<br />

## 🗂️ 데이터 분석 및 시각화
### 뉴스 기사량과 주식의 상관관계
- (대표 시각화 자료 한두개)
- (설명 한줄)

### 뉴스 데이터와 주식의 등락에 대한 상관관계 분석
- (대표 시각화 자료 한두개)
- (설명 한줄)

### 주식과 뉴스 데이터의 감성분석 상관관계 및 키워드 시각화
- (대표 시각화 자료 한두개)
- (설명 한줄)

### 특정구간에서의 특이점 파악
- (대표 시각화 자료 한두개)
- (설명 한줄)
<br />


## 💭 결론
- 뉴스 데이터로 주식 시장 경향을 완전히 분석하기엔 한계가 존재함.
- 하지만, 뉴스 키워드와 감성 분석 결과는 보조 지표로서의 충분한 역할을 함.

