
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

###  🍎문제 인식🍎
#### 사과 값 폭등
![image](https://github.com/addinedu-ros-5th/eda-repo-2/assets/70615068/bd16d942-f005-4c98-a0f8-389af876bcbe)

<div align=center> 
  2024년 1분기 뉴스 발췌
</div> 

### 🧅문제 분석🧅
#### 문제 정의 타당성 검증 필요
단순히 물가가 큰 폭으로 상승한 경우, **사과 값 폭등**을 문제로 설정하는 것은 무의미하다. 

#### 소비자 물가 및 과실류 기여도 확인
문제 정의 타당성 검증을 위해 물가 상승세에 맞추어 사과값이 폭등하였는지 확인해야한다.  
따라서 **소비자 물가**와 **과실류 기여도**를 확인하여  
사과값 폭등을 문제로 인식하고, 이를 분석하는 것이 의미있을지 판단한다.  

#### 10년간 전국 소비자 물가 지수
- 2014년부터 2023년까지 전국 소비자 물가 지수 변화 시각화
- 2020년 이후부터 우상향 그래프 지속
- 기준대비 작년(2023년) 증가폭 최대 (**11.59%**)   
- 기준: 2020년 (=100)
    
<p align="center">

![연도별 전국 소비자 물가 지수](https://github.com/addinedu-ros-5th/eda-repo-2/assets/113625699/453626f2-f349-4156-b985-d491da65aff7)

</p>

<div align=center> 
  전국 과일 물가 지수 [1]
</div> 

#### 10년간 전국 소비자 물가 지수
- 2014년부터 2023년까지 전국 과일 물가 지수 변화 시각화
- 소비자 물가 지수 그래프 양상과 동일
- 기준대비 작년(2023년) 증가폭 최대 (**29.54%**)  
- 기준: 2020년 (=100)
    
<p align="center">

![연도별 전국 과일 물가 지수](https://github.com/addinedu-ros-5th/eda-repo-2/assets/113625699/8f812169-5511-448b-8aca-daa654f7d1b8)

</p>

<div align=center> 
  전국 과일 물가 지수 [1]
</div> 

24년 1월 과실류 기여도: 0.4%P  
→ 전체 소비자물가지수 상승률 2.8%의 7분의 1  
→ 일반적으로 과실류 물가 기여도가 0.1~0.2%P 수준  
→ 최소 **2배 이상 물가 상승에 기여**  
→ 사과 값 폭등 현상은 **문제로 정의 및 분석하기에 적합**  
→ 단, '과실류'가 물가 상승에 0.4% 기여하였으므로, **세부 품목 분석** 필요 

#### 물가 증가 채소 및 과일 파악
문제 상황에 대한 세부 분석을 통해 문제 범위를 좁힌다.  
따라서 물가 상승에 기여한 과실류, 그리고 채소류의 **품목별 물가 파악**이 필요하다. 

#### 채소 품목별 물가 증가율 상위 5위 누적 빈도수
- 2015년부터 2023년까지 물가 상승 상위 5위 품목을 연단위로 누적 시각화
- 상위 품목: 무, 감자, 당근, 배추, 양파 등 
    
<p align="center">

![높은 물가 증가율 상위 5개 품목(채소)](https://github.com/addinedu-ros-5th/eda-repo-2/assets/113625699/6a9dc61b-4f1f-4737-a34f-4f66efb04062)

</p>

<div align=center> 
  채소 품목별 물가 상승 상위 5위 누적 횟수 [2]
</div> 



#### 과일 품목별 물가 증가율 상위 5위 누적 빈도수
- 2015년부터 2023년까지 물가 상승 상위 5위 품목을 연단위로 누적 시각화
- 상위 품목: 귤, 사과, 수박, 감, 배 등 
    
<p align="center">

![높은 물가 증가율 상위 5개 품목(과일)](https://github.com/addinedu-ros-5th/eda-repo-2/assets/113625699/f8c6eadf-a7c6-4446-9b5c-3669ef101bfc)

</p>  

<div align=center> 
  과일 품목별 물가 상승 상위 5위 누적 횟수 [2]
</div> 

#### 분기별 농산물 물가 증감률
- 내용입력
- 내용입력
- 내용입력
    
<p align="center">

![2023년 1분기 품목별 증감률](https://github.com/addinedu-ros-5th/eda-repo-2/assets/163802905/f35dbf27-bb32-4d08-990c-5d45c3147d63)

</p>

<div align=center> 
  2023년 분기별 농산물 물가 [2]
</div>  

#### 기간별 국산 과일 가격 인상
- 내용입력
- 내용입력
- 내용입력
    
<p align="center">

![1년 전(2023) 1개월 전(2024.02) 과일 가격 비교](https://github.com/addinedu-ros-5th/eda-repo-2/assets/163802905/7534f4fe-ffbc-4c4e-8848-833d5f15411e)

</p>  


<div align=center> 
  표 제목 선정  [2]
</div>  

과실류 품목 분석 결과 사과가 물가 상승 최상위 품목 중 하나임을 확인.  
→ 단, 해당 품목의 가격 상승이 **소비자에게 영향이 없다면** 문제 정의 무의미.  
→ **물가 상승에 따른 과실 소비 시장 분석** 필요 

#### 물가 증가에 따른 현상 파악
물가 상승에 따른 과실 **소비 유형 변화** 확인 필요  
→ **물가 상승에 따른 과실 소비 시장 분석** 필요

#### 생과일 및 냉동과일 수입 물량 추이 (딸기)
- 내용 입력
- 내용 입력

<p align="center">

![생 vs 냉동 수입량 비교](https://github.com/addinedu-ros-5th/eda-repo-2/assets/113625699/ce8154c9-5e1d-4b62-b6b3-1e02133584f7)

</p> 

<div align=center> 
  생과일 및 냉동과일 수입 물량 [3][4]
</div>  


#### 생과일 및 건조과일 수입 물량 추이 (사과)
- 내용 입력
- 내용 입력
<p align="center">

![생 vs 건조 수입량 비교](https://github.com/addinedu-ros-5th/eda-repo-2/assets/113625699/24e10851-f9b0-4699-a09e-065744758cb6)

</p> 

<div align=center> 
  생과일 및 건조 과일 수입 물량 [5][6]
</div>  


과실류 품목 소비 시장 분석을 수입 물량 추이를 통해 간접 판단.  
→ 과실류 물가 상승 시기와 대체품 수입 상승 시기가 **유사한 추이**를 보임.  
→ **과실 물가 상승이 소비자에게 영향이 있다**고 판단.  
→ 과실 물가 상승 문제는 **분석 대상으로 적절**하다고 판단.  
→ 해당 문제에 관한 **원인 도출** 필요.

### 🍐원인 도출🍐
이전과 이어지게끔 이야기.  
→ 논리 전개.  
→ 해야할 것 - 시각화 할 내용과 연결.

#### 고령화
##### 제목
- 내용 입력
- 내용 입력
<p align="center">

 ![연령별 장래 인구수](https://github.com/addinedu-ros-5th/eda-repo-2/assets/163129674/a1bf842e-57d9-4125-ba4a-9e53394e62c5)

</p>

<div align=center> 
  연령별 인구수 통계  [출처 번호]
</div>  

#### 제목
- 내용 입력
- 내용 입력
<p align="center">

 ![시도별 고령화비율](https://github.com/addinedu-ros-5th/eda-repo-2/assets/163129674/37409c97-bb29-4de3-8976-2fbad15b668c)

</p>

<div align=center> 
  그래프 제목  [출처 번호]
</div>  


#### 제목
- 내용 입력
- 내용 입력
<p align="center">

![농가인구수](https://github.com/addinedu-ros-5th/eda-repo-2/assets/163129674/e863217f-7751-44c4-b6b2-0c52875bae34)

</p>

<div align=center> 
  그래프 제목  [출처 번호]
</div>

#### 제목
- 내용 입력
- 내용 입력
<p align="center">

![농가인구 고령화비율](https://github.com/addinedu-ros-5th/eda-repo-2/assets/163129674/1da46e5f-fd99-4259-b613-fd30f3cbf330)

</p>

<div align=center> 
  그래프 제목  [출처 번호]
</div>  

#### 제목
- 내용 입력
- 내용 입력
<p align="center">

![1차 산업 숙련종사자수](https://github.com/addinedu-ros-5th/eda-repo-2/assets/163129674/4ec810b3-bebc-4bcb-b36b-fa5f586df9fc)

</p>

<div align=center> 
  그래프 제목  [출처 번호]
</div>  

#### 제목
- 내용 입력
- 내용 입력
<p align="center">

![농가인구수](https://github.com/addinedu-ros-5th/eda-repo-2/assets/163129674/e863217f-7751-44c4-b6b2-0c52875bae34)

</p>

<div align=center> 
  그래프 제목  [출처 번호]
</div>  


#### 이상기후
#### 제목
- 내용 입력
- 내용 입력
<p align="center">
  
  ![2014_2023_전국_시도별_논밭_경지면적_변화추이_꺾은선](https://github.com/addinedu-ros-5th/eda-repo-2/assets/108911726/890e1529-7cc8-4b50-a101-ad2468989df5)

</p>

<div align=center> 
  그래프 제목  [출처 번호]
</div>  


#### 제목
- 내용 입력
- 내용 입력
<p align="center">
  **권역별 배 농지 규모 변화** 링크가 없습니다.
</p>

<div align=center> 
  그래프 제목  [출처 번호]
</div>  


#### 제목
- 내용 입력
- 내용 입력
<p align="center">
   **권역별 사과 농지 규모 변화**의 유효한 링크가 없습니다.
</p>

<div align=center> 
  그래프 제목  [출처 번호]
</div>

#### 제목
- 내용 입력
- 내용 입력
<p align="center">
   **권역별 양파 농지 규모 변화**의 유효한 링크가 없습니다.
</p>

<div align=center> 
  그래프 제목  [출처 번호]
</div>

#### 제목
- 내용 입력
- 내용 입력
<p align="center">

  ![1990_2023_강원_경상_사과_재배면적](https://github.com/addinedu-ros-5th/eda-repo-2/assets/108911726/29644ffe-e0f1-412c-9d46-8c4d681749de)

</p>

<div align=center> 
  그래프 제목  [출처 번호]
</div>

#### 제목
- 내용 입력
- 내용 입력
<p align="center">

  ![2010_2023_수도_강원_양파_변화추이](https://github.com/addinedu-ros-5th/eda-repo-2/assets/108911726/e6f52c1f-b11b-4f52-bdea-01a0b87704bb)

</p>

<div align=center> 
  그래프 제목  [출처 번호]
</div>

#### 제목
- 내용 입력
- 내용 입력
<p align="center">

  ![1980_2020_연평균기온_꺾은선](https://github.com/addinedu-ros-5th/eda-repo-2/assets/108911726/63582075-cbd1-475f-b08b-85710fbc4464)

</p>

<div align=center> 
  그래프 제목  [출처 번호]
</div>

#### 제목
- 내용 입력
- 내용 입력
<p align="center">

![1905_2040_시계열_예측_1](https://github.com/addinedu-ros-5th/eda-repo-2/assets/108911726/ee8f64cb-4468-4576-8bbb-4ac93f9eb2ed)

</p>

<div align=center> 
  그래프 제목  [출처 번호]
</div>


분석 결과 이야기.  
→ 논리 전개.  
→ 해야할 것 - 이후의 내용과 연결.

### 💡해결책 제시💡
이전과 이어지게끔 이야기.  
논리 전개.  
해야할 것 - 시각화 할 내용과 연결.
#### 스마트팜
- 내용 입력
- 내용 입력

#### 제목
- 내용 입력
- 내용 입력
<p align="center">

   ![스마트팜 구글 트랜드 분석](https://github.com/addinedu-ros-5th/eda-repo-2/assets/113625699/dbb74260-62a7-494a-be47-789b11896893)

</p>

<div align=center> 
  스마트팜 트랜드 분석  [16]
</div>

#### 스마트팜 제시 근거
스마트팜 내용입력  
→ 스마트팜 내용입력

<p align="center">

  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/70615068/209df21e-4ae3-4b8f-a9ae-06348246e4ca" alt="Image 1" style="width:49%;">
  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/70615068/dfd95f98-a5e3-4125-9dbc-f49154889da7" alt="Image 2" style="width:49%;">

</p>


<div align=center> 
  스마트팜 도입시 생산량 및 순수입 변화 [17]
</div>


스마트팜 내용입력  
→ 스마트팜 내용입력

### 출처
- 1: [품목별 소비자물가지수-통계청](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1ET0017)

- 2: [소매가격-농산물유통정보](https://www.kamis.or.kr/customer/main/main.do)

- 3:[한국무역통계진흥원,생딸기, 검색순서:과실·견과류→0810→081010→[0810100000]](https://www.bandtrass.or.kr/customs/total.do?command=CUS001View&viewCode=CUS00201)

- 4:[한국무역통계진흥원, 냉동딸기, 검색순서: 과실·견과류→0811→081110→[0811100000]](https://www.bandtrass.or.kr/customs/total.do?command=CUS001View&viewCode=CUS00201)

- 5: [한국무역통계진흥원, 생사과, 검색순서:과실·견과류→0808→080810→[0808100000]](https://www.bandtrass.or.kr/customs/total.do?command=CUS001View&viewCode=CUS00201)

- 6: [한국무역통계진흥원,  건조사과, 검색순서:과실·견과류→0813→081330→[0813300000]](https://www.bandtrass.or.kr/customs/total.do?command=CUS001View&viewCode=CUS00201)


- 7: [채소생산량(과채류).통계청](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1ET0027&vw_cd=MT_ZTITLE&[…]th=MT_ZTITLE&path=%252FstatisticsList%252FstatisticsListIndex.do)

- 8: [통계청. 『[장래인구]성 및 연령별 추계인구/전국) 1960-2023』](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1BPA001&vw_cd=MT_ZTITLE&[…]th=MT_ZTITLE&path=%252FstatisticsList%252FstatisticsListIndex.do)

- 9: [통계청. 『고령인구비율(시도/시/군/구) 2000-2023』](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1YL20631&conn_path=I2) 

- 10: [통계청. 『[농가인구수]행정구역별 농가인구』](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1EA1011&vw_cd=MT_ZTITLE&[…]th=MT_ZTITLE&path=%252FstatisticsList%252FstatisticsListIndex.do)

- 11: [통계청. 『[농가인구 고령화비율]』](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1EA1011&vw_cd=MT_ZTITLE&[…]th=MT_ZTITLE&path=%252FstatisticsList%252FstatisticsListIndex.do)

- 12 링크 수정 필요: [통계청. 『1차 산업숙련 종사자수』](https://kosis.kr/index/index.do)

- 13: [전국(도별) 논밭별 경지면적.통계청](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1ET0027&vw_cd=MT_ZTITLE&[…]th=MT_ZTITLE&path=%252FstatisticsList%252FstatisticsListIndex.do)

- 14: [전국 기후변화 시나리오.기상청.](http://www.climate.go.kr/home/CCS/regionclimate/main_view.html)

- 15: [과거관측-일별자료-기상청 날씨누리](https://www.weather.go.kr/w/obs-climate/land/past-obs/obs-by-day.do?stn=108&yy=2005&mm=3&obs=1)

-  16: [스마트팜 구글 트랜드 분석](https://trends.google.com/trends/explore?date=2020-02-20%202024-03-20&geo=KR&q=%EC%8A%A4%EB%A7%88%ED%8A%B8%ED%8C%9C)

- 17: [농림축산식품부.(2023). ***『스마트농업 실태조사』*** n.p.: 농림축산식품부. pp121-122](https://www.smartfarmkorea.net/file/download.do;jsessionid=AK3Mg84InUsxoe9loLVYtG4Dsi1LPJh9DsX7YRkkCdLy1wVazSOSFqg2ag3I8a2s.ICTfusionwas2_servlet_smffront?fileId=3365&type=BBS)