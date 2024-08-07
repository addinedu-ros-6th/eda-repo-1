# 의료 로봇 섹터 뉴스 데이터 감성 분석을 통한 주식 시장 경향 분석
  
***과연 뉴스 데이터의 긍정-부정 수치를 보고 주식 매도-매수를 해도 될까?*** <br>
***뉴스 데이터와 주식 시장 경향에 유의미한 연관성이 있을까?***


## 🤖 프로젝트 소개
- 본 프로젝트는 뉴스 기사의 정서와 그것이 주가에 미치는 영향을 분석함으로써 시장 행동과 일반적인 투자 전략의 타당성에 대한 더 깊은 이해를 제공하는 것을 목표

## 🧠 구성원 및 역할
|이름|업무|
|:---|:---|
|고선민|- 미국 섹터 Google 웹크롤링 및 전처리 <br> - pipeline을 통한 미국기사 감성분석 <br> - plotly를 통한 주식과 뉴스 데이터의 감성분석 상관관계 및 키워드 시각화|
|강지훈|- 한국 섹터 Naver 웹크롤링 및 데이터 전처리 <br> - yfinance를 통한 기업별 평균 종가 데이터 시각화  <br> - 뉴스 기사량과 주식의 상관관계 분석|
|김주영|- 한국 섹터 Naver 웹크롤링 <br> - 주식 시작 경향 파악 및 데이터 수집 <br> - 종목별 특정 구간에서의 이동평균선 특이점 분석 및 시각화|
|이세형|- Roberta DL 모델을 활용한 자연어 학습 및 감성분석 <br> - DB 구축, 관리, 및 Query 작성 <br> - 뉴스데이터와 주식의 등락에 대한 상관관계 분석|

## 🖥️ 활용 기술
|구분|상세|
|:---|:---|
|개발환경|<img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white" /> |
|IDE| <img src="https://img.shields.io/badge/VSCode-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white" /> <img src="https://img.shields.io/badge/Jupyter-F37626.svg?&style=for-the-badge&logo=Jupyter&logoColor=white" /> <img src="https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252" />|
|언어| <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />   |
|EDA 시각화|<img src="https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white" /> <img src="https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white" /> <img src="https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white" /> <img src="https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black" /> ![yahoo-news (1)](https://github.com/user-attachments/assets/fc51c1aa-3dd5-4732-b0cd-a7d45777c51f)|
|웹 크롤링| <img src="https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=Selenium&logoColor=white" /> Newspaper3k| 
|DB|<img src="https://img.shields.io/badge/Amazon_RDS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white" /> <img src="https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white" />|
|협업|<img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" /> <img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white" /> <img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white" /> |
