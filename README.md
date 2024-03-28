
# <div align="center"> 🧅🍎농산물 가격 폭등의 원인 분석 및 해결책 탐구🍎🧅</div>


##### <div align="center">Analyzing the Causes and Exploring Solutions for the Surge in Agricultural Commodity Prices</div>



## 프로젝트 개요  🍎🍐🧅
### 파이썬 모듈 기반 정보 수집, 시계열 예측, DB 관리 및 시각화를 통한
### 농산물 가격 상승 현상에 대한 원인 분석 및 가격 안정화 솔루션 제시

<img src="https://raw.githubusercontent.com/JangHyeongJun-0523/EDA_Project/main/AutoFarmingFlowChart.webp"> 

### 👥 팀원 소개 👥
<img src="https://raw.githubusercontent.com/JangHyeongJun-0523/EDA_Project/main/TeamRole.webp"> 

<hr>

### 📚기술 스택📚
<div align=center> 
    <img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white"> 
    <img src="https://img.shields.io/badge/jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white"> 
    <img src="https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=white"> 
    <img src="https://img.shields.io/badge/amazonaws-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white">
    <br>
    <img src="https://img.shields.io/badge/prophet-6236FF?style=for-the-badge&logo=prophet&logoColor=white">
    <img src="https://img.shields.io/badge/folium-77B829?style=for-the-badge&logo=folium&logoColor=white">
    <img src="https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white">
    <img src="https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy&logoColor=white">
    <img src="https://img.shields.io/badge/selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white">
    <img src="https://img.shields.io/badge/beautifulsope-150458?style=for-the-badge&logo=beautifulsope&logoColor=white">
    <br>
    <hr>
</div>  

### 💬협업 툴💬
  <div align=center> 
    <img src="https://img.shields.io/badge/git-F05032?style=for-the-badge&logo=git&logoColor=white">
    <img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white">
    <img src="https://img.shields.io/badge/slack-4A154B?style=for-the-badge&logo=slack&logoColor=white">
    <img src="https://img.shields.io/badge/figjam-F24E1E?style=for-the-badge&logo=figma&logoColor=white">
</div>


---
## 📊 탐색적 데이터 분석 📊

###  🍎1. 문제 인식🍎
#### 1-1.  사과 값 폭등
<img src="https://private-user-images.githubusercontent.com/70615068/317709529-bd16d942-f005-4c98-a0f8-389af876bcbe.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE2MzM1MDEsIm5iZiI6MTcxMTYzMzIwMSwicGF0aCI6Ii83MDYxNTA2OC8zMTc3MDk1MjktYmQxNmQ5NDItZjAwNS00Yzk4LWEwZjgtMzg5YWY4NzZiY2JlLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAzMjglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMzI4VDEzNDAwMVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWFkZmE0N2M4MTY3MmIyNGYyMzI3ZGZkM2RlNjBjMWY0NzQ0NTY4YWUzZDUyNzU5OGQ4NmMwMGUzOGEyNmUxYTMmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.7CvHUhdXwhArf0Eii9RFOMrbBUcbR-4cxsmp0iRB12g">
<center>2024년 1분기 뉴스 토픽</center>

### 🧅2. 문제 분석🧅
#### 2-1. 문제 정의 타당성 검증 필요
단순히 물가가 큰 폭으로 상승한 경우, **사과 값 폭등**을 문제로 설정하는 것은 무의미하다. 

#### 2-2. 소비자 물가 및 과실류 기여도 확인
문제 정의 타당성 검증을 위해 물가 상승세에 맞추어 사과값이 폭등하였는지 확인해야한다.  
따라서 **소비자 물가**와 **과실류 기여도**를 확인하여  
사과값 폭등을 문제로 인식하고, 이를 분석하는 것이 의미있을지 판단한다.  

#### 2-2-1. 10년간 전국 소비자 물가 지수
- 2014년부터 2023년까지 전국 소비자 물가 지수 변화 시각화
- 2020년 이후부터 우상향 그래프 지속
- 기준대비 작년(2023년) 증가폭 최대 (**11.59%**)   
- 기준: 2020년 (=100)
    
<p align="center">
<img src="https://private-user-images.githubusercontent.com/113625699/316791362-453626f2-f349-4156-b985-d491da65aff7.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE2MzMyMTgsIm5iZiI6MTcxMTYzMjkxOCwicGF0aCI6Ii8xMTM2MjU2OTkvMzE2NzkxMzYyLTQ1MzYyNmYyLWYzNDktNDE1Ni1iOTg1LWQ0OTFkYTY1YWZmNy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwMzI4JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDMyOFQxMzM1MThaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0zNjFiZDJiNWYzMzZhNTliYTk1NzdmZDNlOTY3OTM1OWU2MTZhNTEyODVmMjJmNGUyNTljYTk1NDU1YWFlYjc4JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.mT3Vtk6ZGyiJrpofxMW_Gj24g9WQ7fG3UtSc8FS_y_4">
<center>전국 소비자 물가 총 지수 [1]</center>
</p>

#### 2-2-2. 10년간 전국 소비자 물가 지수
- 2014년부터 2023년까지 전국 과일 물가 지수 변화 시각화
- 소비자 물가 지수 그래프 양상과 동일
- 기준대비 작년(2023년) 증가폭 최대 (**29.54%**)  
- 기준: 2020년 (=100)
    
<p align="center">
<img src="https://private-user-images.githubusercontent.com/113625699/316791352-8f812169-5511-448b-8aca-daa654f7d1b8.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE2MzMyMTgsIm5iZiI6MTcxMTYzMjkxOCwicGF0aCI6Ii8xMTM2MjU2OTkvMzE2NzkxMzUyLThmODEyMTY5LTU1MTEtNDQ4Yi04YWNhLWRhYTY1NGY3ZDFiOC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwMzI4JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDMyOFQxMzM1MThaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0xMGM2OGMwNTcxNTkyZTA1Y2ZkOWVmZWJjMmY0NGZiMmFiNzU1NzU5YWM4ZTg4YmViYmYwZjFlOGVmM2YwMTJjJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.YGQKQ4sKix9r8eMIX5hYqhntG4RMBddhkVuApnhx1hI">
<center>전국 과일 물가 지수 [1]</center>
</p>


24년 1월 과실류 기여도: 0.4%P  
→ 전체 소비자물가지수 상승률 2.8%의 7분의 1  
→ 일반적으로 과실류 물가 기여도가 0.1~0.2%P 수준  
→ 최소 **2배 이상 물가 상승에 기여**  
→ 사과 값 폭등 현상은 **문제로 정의 및 분석하기에 적합**  
→ 단, '과실류'가 물가 상승에 0.4% 기여하였으므로, **세부 품목 분석** 필요 

#### 2-3. 물가 증가 채소 및 과일 파악
문제 상황에 대한 세부 분석을 통해 문제 범위를 좁힌다.  
따라서 물가 상승에 기여한 과실류, 그리고 채소류의 **품목별 물가 파악**이 필요하다. 

#### 2-3-1. 채소 품목별 물가 증가율 상위 5위 누적 빈도수
- 2015년부터 2023년까지 물가 상승 상위 5위 품목을 연단위로 누적 시각화
- 상위 품목: 무, 감자, 당근, 배추, 양파 등 
    
<p align="center">
<img src="https://private-user-images.githubusercontent.com/113625699/316792233-6a9dc61b-4f1f-4737-a34f-4f66efb04062.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE2MzMyNjgsIm5iZiI6MTcxMTYzMjk2OCwicGF0aCI6Ii8xMTM2MjU2OTkvMzE2NzkyMjMzLTZhOWRjNjFiLTRmMWYtNDczNy1hMzRmLTRmNjZlZmIwNDA2Mi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwMzI4JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDMyOFQxMzM2MDhaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hOTFjYjExYzU5ZmNhNDE2YTdkYWU5MGQ0YmQ2MGY1NWI5NGY4ZDJkYmY0ZDJmNWNlMzM1YWVkNjg2NmFiM2UzJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.a3ZMMWDhe_XTX9JjuLm6_BwePZeCDZIRpOFvC_AkYPs">
<center>채소 품목별 물가 상승 상위 5위 누적 횟수 [2]</center>
</p>



#### 2-3-2. 과일 품목별 물가 증가율 상위 5위 누적 빈도수
- 2015년부터 2023년까지 물가 상승 상위 5위 품목을 연단위로 누적 시각화
- 상위 품목: 귤, 사과, 수박, 감, 배 등 
    
<p align="center">
<img src="https://private-user-images.githubusercontent.com/113625699/316792229-f8c6eadf-a7c6-4446-9b5c-3669ef101bfc.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE2MzMyNjgsIm5iZiI6MTcxMTYzMjk2OCwicGF0aCI6Ii8xMTM2MjU2OTkvMzE2NzkyMjI5LWY4YzZlYWRmLWE3YzYtNDQ0Ni05YjVjLTM2NjllZjEwMWJmYy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwMzI4JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDMyOFQxMzM2MDhaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT03MGU5YjQxMWEyM2U1NzdhYjk4YTcxOTgxOTViYTBiNjAxODZmMzMwMjczOTA3M2EyNTYxZWIxMGQzNGQwODNiJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.wWMwjaUksWzfh3vhOMAWvcGv72mOCwx0E97INmRQJCE">
<center>과일 품목별 물가 상승 상위 5위 누적 횟수 [2]</center>  
</p>  

#### 2-3-3. 분기별 농산물 물가 증감률
- 내용입력
- 내용입력
- 내용입력
    
<p align="center">
<img src="https://private-user-images.githubusercontent.com/163802905/316788759-f35dbf27-bb32-4d08-990c-5d45c3147d63.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE2MzU4NzgsIm5iZiI6MTcxMTYzNTU3OCwicGF0aCI6Ii8xNjM4MDI5MDUvMzE2Nzg4NzU5LWYzNWRiZjI3LWJiMzItNGQwOC05OTBjLTVkNDVjMzE0N2Q2My5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwMzI4JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDMyOFQxNDE5MzhaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT02ZDEwMTllZjc4ZjExNzRhOTk1NzA1OTBhNjUxOTdjNzYxOWZkMmYwM2U3YTNkY2E0YjdmZmUxZTJlZGNlN2I2JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.i6Sg7afc637wo5WEgyhM2N8QATs7_bTyeGZUmxTN5Z8">
<center>2023년 분기별 농산물 물가 [2]</center>  
</p>  

#### 2-3-4. 기간별 국산 과일 가격 인상
- 내용입력
- 내용입력
- 내용입력
    
<p align="center">
<img src="https://private-user-images.githubusercontent.com/163802905/316788906-7534f4fe-ffbc-4c4e-8848-833d5f15411e.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE2MzU4NzgsIm5iZiI6MTcxMTYzNTU3OCwicGF0aCI6Ii8xNjM4MDI5MDUvMzE2Nzg4OTA2LTc1MzRmNGZlLWZmYmMtNGM0ZS04ODQ4LTgzM2Q1ZjE1NDExZS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwMzI4JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDMyOFQxNDE5MzhaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0yNGViY2QxMzQxYTcwMGE1M2RkNWQ2OGIxMmRjYWU4YzExMDVkYjIzZjQyZTUzZmYxNzU2M2YzNGQzNzc2Y2FhJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.b8U9GWnmH6oist_2pyBxuvolBRMHbcgVIwviCLDKqbg">
<center>표 제목 선정  [2]</center>  
</p>  

과실류 품목 분석 결과 사과가 물가 상승 최상위 품목 중 하나임을 확인.  
→ 단, 해당 품목의 가격 상승이 **소비자에게 영향이 없다면** 문제 정의 무의미.  
→ **물가 상승에 따른 과실 소비 시장 분석** 필요 

#### 2-4. 물가 증가에 따른 현상 파악
물가 상승에 따른 과실 **소비 유형 변화** 확인 필요  
→ **물가 상승에 따른 과실 소비 시장 분석** 필요

#### 2-4-1. 생과일 및 냉동과일 수입 물량 추이
- 내용 입력
- 내용 입력
<p align="center">
<img src="https://private-user-images.githubusercontent.com/113625699/316793519-ce8154c9-5e1d-4b62-b6b3-1e02133584f7.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE2MzQyOTksIm5iZiI6MTcxMTYzMzk5OSwicGF0aCI6Ii8xMTM2MjU2OTkvMzE2NzkzNTE5LWNlODE1NGM5LTVlMWQtNGI2Mi1iNmIzLTFlMDIxMzM1ODRmNy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwMzI4JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDMyOFQxMzUzMTlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1kYzRjZDIyMTM5NTgzOThlZTEwMjAxMzhiMmU5MzAyY2JmYzA4MTY0YmQ1ODU3MDk3YzQ1NDk1YTg4Mzk5MDI5JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.VVFstHno4vzri7a6hPdJzdU7v-W92b3ZE4AV0cYor1I">
<center>생과일 및 냉동과일 수입 물량 [?]</center>  
</p> 

#### 2-4-2. 생과일 및 건조과일 수입 물량 추이
- 내용 입력
- 내용 입력
<p align="center">
<img src="https://private-user-images.githubusercontent.com/113625699/316794038-24e10851-f9b0-4699-a09e-065744758cb6.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE2MzQyOTksIm5iZiI6MTcxMTYzMzk5OSwicGF0aCI6Ii8xMTM2MjU2OTkvMzE2Nzk0MDM4LTI0ZTEwODUxLWY5YjAtNDY5OS1hMDllLTA2NTc0NDc1OGNiNi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwMzI4JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDMyOFQxMzUzMTlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0xNzg4YjZmZmQzMTJmYzc1NTdiOGE0YWM4ZTNmYzIyNTc2YzY0YWFmNzBjODU0NGIwYTI2NDY3MWY1ZWNjOWE5JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.gGu8BdFnrB-aGGeOCImjXWIK45CF7o7vDgCIbVFWpGM">
<center>생과일 및 건조과일 수입 물량 [?]</center>  
</p> 

과실류 품목 소비 시장 분석을 수입 물량 추이를 통해 간접 판단.  
→ 과실류 물가 상승 시기와 대체품 수입 상승 시기가 **유사한 추이**를 보임.  
→ **과실 물가 상승이 소비자에게 영향이 있다**고 판단.  
→ 과실 물가 상승 문제는 **분석 대상으로 적절**하다고 판단.  
→ 해당 문제에 관한 **원인 도출** 필요.

### 🍐3. 원인 도출🍐
이전과 이어지게끔 이야기.  
→ 논리 전개.  
→ 해야할 것 - 시각화 할 내용과 연결.

#### 3-1.고령화
#### 3-1-1. 제목
- 내용 입력
- 내용 입력
<p align="center">
<img src="이미지주소">
<center>표 제목 선정  [출처 번호]</center>  
</p>  

#### 3-2.이상기후
#### 3-2-1. 제목
- 내용 입력
- 내용 입력
<p align="center">
<img src="이미지주소">
<center>표 제목 선정  [출처 번호]</center>  
</p>  

#### 3-2-2. 제목
- 내용 입력
- 내용 입력
<p align="center">
<img src="이미지주소">
<center>표 제목 선정  [출처 번호]</center>  
</p>  

#### 3-2-3. 제목
- 내용 입력
- 내용 입력
<p align="center">
<img src="이미지주소">
<center>표 제목 선정  [출처 번호]</center>  
</p>  

분석 결과 이야기.  
→ 논리 전개.  
→ 해야할 것 - 이후의 내용과 연결.

### 💡4. 해결책 제시💡
이전과 이어지게끔 이야기.  
→ 논리 전개.  
→ 해야할 것 - 시각화 할 내용과 연결.
#### 4-1. 스마트팜
- 내용 입력
- 내용 입력

#### 4-2. 스마트팜 제시 근거
스마트팜 내용입력  
→ 스마트팜 내용입력

<p align="center">
  <img src="https://private-user-images.githubusercontent.com/70615068/316704670-209df21e-4ae3-4b8f-a9ae-06348246e4ca.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE2MzMzMzYsIm5iZiI6MTcxMTYzMzAzNiwicGF0aCI6Ii83MDYxNTA2OC8zMTY3MDQ2NzAtMjA5ZGYyMWUtNGFlMy00YjhmLWE5YWUtMDYzNDgyNDZlNGNhLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAzMjglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMzI4VDEzMzcxNlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTQ4NjBjY2Y0OWFhYWMwN2E3OWJiMzEwMDM3ZGE2ZGQ5YWE0MWM4NDdlZDM4MWRmMDQzYjYxZjk0MDI4YmE4YzUmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.CBFRsg8cjLQcVrmsJF9d561tL6lkX7XBD3B1GHdHruQ" width="49%">
  <img src="https://private-user-images.githubusercontent.com/70615068/316704721-dfd95f98-a5e3-4125-9dbc-f49154889da7.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE2MzMzMzYsIm5iZiI6MTcxMTYzMzAzNiwicGF0aCI6Ii83MDYxNTA2OC8zMTY3MDQ3MjEtZGZkOTVmOTgtYTVlMy00MTI1LTlkYmMtZjQ5MTU0ODg5ZGE3LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAzMjglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMzI4VDEzMzcxNlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWNmY2NkZTBkZmIwMzJlMWZlMTlkMzljZmJmYzZmNWRhOTgzZDgyYTgxYzdmMDhjMTBlOTE0ZTEyYjY1YjdhNGImWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.9zO9PDX2km2gFWp--viPwbsAPHcklit8LCVMQ8Hl3rI" width="49%">
  <center>스마트팜 도입시 생산량 및 순수입 변화 [12]</center>
</p>

스마트팜 내용입력  
→ 스마트팜 내용입력

### 출처
- 1: [품목별 소비자물가지수-통계청](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1ET0017)

- 2: [소매가격-농산물유통정보](https://www.kamis.or.kr/customer/main/main.do)

- 3: [채소생산량(과채류).통계청](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1ET0027&vw_cd=MT_ZTITLE&[…]th=MT_ZTITLE&path=%252FstatisticsList%252FstatisticsListIndex.do)

- 4: [통계청. 『[장래인구]성 및 연령별 추계인구/전국) 1960-2023』](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1BPA001&vw_cd=MT_ZTITLE&[…]th=MT_ZTITLE&path=%252FstatisticsList%252FstatisticsListIndex.do)

- 5: [통계청. 『고령인구비율(시도/시/군/구) 2000-2023』](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1YL20631&conn_path=I2) 

- 6: [통계청. 『[농가인구수]행정구역별 농가인구』](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1EA1011&vw_cd=MT_ZTITLE&[…]th=MT_ZTITLE&path=%252FstatisticsList%252FstatisticsListIndex.do)

- 7: [통계청. 『[농가인구 고령화비율]』](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1EA1011&vw_cd=MT_ZTITLE&[…]th=MT_ZTITLE&path=%252FstatisticsList%252FstatisticsListIndex.do)

- 8 링크 수정 필요: [통계청. 『1차 산업숙련 종사자수』](https://kosis.kr/index/index.do)

- 9: [전국(도별) 논밭별 경지면적.통계청](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1ET0027&vw_cd=MT_ZTITLE&[…]th=MT_ZTITLE&path=%252FstatisticsList%252FstatisticsListIndex.do)

- 10: [전국 기후변화 시나리오.기상청.](http://www.climate.go.kr/home/CCS/regionclimate/main_view.html)

- 11: [과거관측-일별자료-기상청 날씨누리](https://www.weather.go.kr/w/obs-climate/land/past-obs/obs-by-day.do?stn=108&yy=2005&mm=3&obs=1)


- 12: [농림축산식품부.(2023). ***『스마트농업 실태조사』*** n.p.: 농림축산식품부. pp121-122](https://www.smartfarmkorea.net/file/download.do;jsessionid=AK3Mg84InUsxoe9loLVYtG4Dsi1LPJh9DsX7YRkkCdLy1wVazSOSFqg2ag3I8a2s.ICTfusionwas2_servlet_smffront?fileId=3365&type=BBS)