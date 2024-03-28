
# <div align="center"> 🧅🍎농산물 가격 폭등의 원인 분석 및 해결책 탐구🍎🧅</div>


##### <div align="center">Analyzing the Causes and Exploring Solutions for the Surge in Agricultural Commodity Prices</div>



## 프로젝트 개요  🍎🍐🧅
### 파이썬 모듈 기반 정보 수집, 시계열 예측 및 시각화를 통한
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
<img src="https://private-user-images.githubusercontent.com/70615068/317709529-bd16d942-f005-4c98-a0f8-389af876bcbe.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE2MjU5MjYsIm5iZiI6MTcxMTYyNTYyNiwicGF0aCI6Ii83MDYxNTA2OC8zMTc3MDk1MjktYmQxNmQ5NDItZjAwNS00Yzk4LWEwZjgtMzg5YWY4NzZiY2JlLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAzMjglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMzI4VDExMzM0NlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTcwMWYxNTA5Y2FhZTU2YjBkYWRlNmQ4OTUwZWE2ZGY1ZjcwYTdmMjk2NzE4YzIwZmEzMDY2NjNlN2U2NDdlMGYmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.XVzKt50E26FPnlrRzOZSlTiwgaka-KZwnLVYGf8UZEY">

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
<img src="https://private-user-images.githubusercontent.com/113625699/316791362-453626f2-f349-4156-b985-d491da65aff7.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE2MjcwNDAsIm5iZiI6MTcxMTYyNjc0MCwicGF0aCI6Ii8xMTM2MjU2OTkvMzE2NzkxMzYyLTQ1MzYyNmYyLWYzNDktNDE1Ni1iOTg1LWQ0OTFkYTY1YWZmNy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwMzI4JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDMyOFQxMTUyMjBaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1kOGFhMjFhNGVmOTI5YTVjMGIxMWY5OTBlOGNkZjk1MTRkNDE0MDI1Mzk5YTY5MGRkYTk5N2Y2YWE4YmE3NjRjJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.lrud5Tlp0cqJPHdNgjQFzlmARMsii-jUQ30rclEXZqk">
  <figcaption align="center"><a align="center">전국 소비자 물가 총 지수 [1]</a></figcaption>
</p>

#### 2-2-2. 10년간 전국 소비자 물가 지수
- 2014년부터 2023년까지 전국 과일 물가 지수 변화 시각화
- 소비자 물가 지수 그래프 양상과 동일
- 기준대비 작년(2023년) 증가폭 최대 (**29.54%**)  
- 기준: 2020년 (=100)
    
<p align="center">
<img src="https://private-user-images.githubusercontent.com/113625699/316791352-8f812169-5511-448b-8aca-daa654f7d1b8.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE2Mjc3MzgsIm5iZiI6MTcxMTYyNzQzOCwicGF0aCI6Ii8xMTM2MjU2OTkvMzE2NzkxMzUyLThmODEyMTY5LTU1MTEtNDQ4Yi04YWNhLWRhYTY1NGY3ZDFiOC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwMzI4JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDMyOFQxMjAzNThaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT03OGUyMjFkODc0NTEwYjRkNGM5OTJjM2VkYTE4YmU4ODdhNzIyNDZjZDQ5ZDhjYjhjOGQxNTdjZGM0MDUzZWVjJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.gug0cLF-JRD2O_SghxwGO5g28mBk6XGtjn5Je1WGSJw">
  <figcaption align="center"><a align="center">전국 과일 물가 지수 [1]</a></figcaption>
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
<img src="https://private-user-images.githubusercontent.com/113625699/316792233-6a9dc61b-4f1f-4737-a34f-4f66efb04062.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE2MjkwNTIsIm5iZiI6MTcxMTYyODc1MiwicGF0aCI6Ii8xMTM2MjU2OTkvMzE2NzkyMjMzLTZhOWRjNjFiLTRmMWYtNDczNy1hMzRmLTRmNjZlZmIwNDA2Mi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwMzI4JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDMyOFQxMjI1NTJaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT00YTBmMjQ0ZTIyZmJlMzQ3ZWJhZjc0YzBhZTdlMmQ4MWU1MjY0ZTAwNjExODM3NGVmM2RiYzkyOWJkMzI3YjM5JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.mQnbxL6VeuYSRdxgZJV7vBxJyH0GVlKcp_vUUV925R8">
  <figcaption align="center"><a align="center">채소 품목별 물가 상승 상위 5위 누적 횟수 [2]</a></figcaption>
</p>

#### 2-3-2. 과일 품목별 물가 증가율 상위 5위 누적 빈도수
- 2015년부터 2023년까지 물가 상승 상위 5위 품목을 연단위로 누적 시각화
- 상위 품목: 귤, 사과, 수박, 감, 배 등 
    
<p align="center">
<img src="https://private-user-images.githubusercontent.com/113625699/316792229-f8c6eadf-a7c6-4446-9b5c-3669ef101bfc.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE2Mjk0NjYsIm5iZiI6MTcxMTYyOTE2NiwicGF0aCI6Ii8xMTM2MjU2OTkvMzE2NzkyMjI5LWY4YzZlYWRmLWE3YzYtNDQ0Ni05YjVjLTM2NjllZjEwMWJmYy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwMzI4JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDMyOFQxMjMyNDZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1iZGRjOGU4NWI4ZGFjZTk5ZjUxN2JkYTg0ZGJkN2QyMTExZDE0Njk3NDYyZGRhNDkyYTk4MjBiOTUxZDI4ZTA2JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.MvTNBlI-mJHDouikE1koMRVXxjKjjy_QCuEl8WZN6Lc">
  <figcaption align="center"><a align="center">과일 품목별 물가 상승 상위 5위 누적 횟수 [2]</a></figcaption>
</p>

과실류 품목 분석 결과 사과가 물가 상승 최상위 품목 중 하나임을 확인.  
→ 단, 해당 품목의 가격 상승이 **소비자에게 영향이 없다면** 문제 정의 무의미.  
→ **물가 상승에 따른 과실 소비 시장 분석** 필요 

#### 2-4. 물가 증가에 따른 현상 파악
물가 상승에 대한 

### 🍐3. 원인 도출🍐

#### 3-1.고령화

#### 3-2.이상기후

### 💡4. 해결책 제시💡
#### 4-1. 
#### 4-2. 스마트팜 제시 근거
스마트팜 농작물 생산량 및 변화율

<p align="center">
  <img src="https://private-user-images.githubusercontent.com/70615068/316704670-209df21e-4ae3-4b8f-a9ae-06348246e4ca.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE1Mjk5ODEsIm5iZiI6MTcxMTUyOTY4MSwicGF0aCI6Ii83MDYxNTA2OC8zMTY3MDQ2NzAtMjA5ZGYyMWUtNGFlMy00YjhmLWE5YWUtMDYzNDgyNDZlNGNhLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAzMjclMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMzI3VDA4NTQ0MVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWM3MTliMWNmMGM3MWY3ODMwMDRhMDFiNzZiNjk5N2JmMmI3OTkwYWEwYTU2YmVjYzRjMWYzYTczMDQ0ZmYwZWYmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.afjI8-w9QB2COKdmOt1P6_ycVCcumsGZFv-pwyTRfFw" width="49%">
  <img src="https://private-user-images.githubusercontent.com/70615068/316704721-dfd95f98-a5e3-4125-9dbc-f49154889da7.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE1Mjk5ODEsIm5iZiI6MTcxMTUyOTY4MSwicGF0aCI6Ii83MDYxNTA2OC8zMTY3MDQ3MjEtZGZkOTVmOTgtYTVlMy00MTI1LTlkYmMtZjQ5MTU0ODg5ZGE3LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAzMjclMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMzI3VDA4NTQ0MVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTFlYWZmOGIyMTNlMzgxZTE2MTZmYzJiMGUwOTYwNjhlOTY5YjRiNGI5MzAwNmRhNGRlYjExMDFmMDI1ODU1NzAmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.cU4GYauH1qc7HxiSidj5riSUQkXjMZiX-218ZLv1cIU" width="49%">
  <figcaption align="center">스마트팜 도입시 생산량 및 순수입 변화 [12]</figcaption>
</p>


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