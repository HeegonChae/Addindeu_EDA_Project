
# <div align="center"> 🧅🍎농산물 가격 폭등의 원인 분석 및 해결책 탐구🍎🧅</div>


##### <div align="center">Analyzing the Causes and Exploring Solutions for the Surge in Agricultural Commodity Prices</div>



## 프로젝트 개요  🍎🍐🧅
### 파이썬 모듈 기반 정보 수집, 시계열 예측, DB 관리 및 시각화를 통한
### 농산물 가격 상승 현상에 대한 원인 분석 및 가격 안정화 솔루션 제시

<img src="https://raw.githubusercontent.com/JangHyeongJun-0523/EDA_Project/main/AutoFarmingFlowChart.webp"> 

### 👥 팀원 소개 👥
<img src="https://raw.githubusercontent.com/JangHyeongJun-0523/EDA_Project/main/TeamRole.webp"> 

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
최근(2024.01) 농산물 등 가격이 얼마나 변화했는지 체감해주는 <b>소비자 물가 지수</b>와 <br/> 
<b>실제 과일 값 폭등</b>에 관련된 기사들을 쉽게 접할 수 있다. 

<div align=center> 
  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/70615068/bd16d942-f005-4c98-a0f8-389af876bcbe" alt="appleNews" style="width:75%;">

  2024년 1분기 뉴스 발췌
</div> 

### 🧅문제 분석🧅
#### 문제 정의
이번 프로젝트에서는 물가 상승 폭 급상승이 아닌 사과, 배 등 <br/>
**농산물 가격 상승 현상에 대한 분석**을 문제 대상으로 설정했다.<br/>


#### 문제 정의 타당성 검증
우선적으로 물가 상승세에 맞춰 과일 값이 폭등하였는지를 분석하고자 한다. <br/>
**소비자 물가**와 **과실류 기여도**를 확인하여 사과값 폭등을 문제로 인식하고, 유효한 의미가 있는지를 판단했다. 

#### 10년간 전국 소비자 물가 지수 및 과일 물가 지수 [1]
- 2014년부터 2023년까지 전국 소비자 물가 및 과일 물가 지수 추이 시각화
- 기준: 2020년 (=100)
    
 <p align="center">

  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/113625699/453626f2-f349-4156-b985-d491da65aff7" alt="Image 1" style="width:49%;">
  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/113625699/8f812169-5511-448b-8aca-daa654f7d1b8" alt="Image 2" style="width:49%;">

</p>   

2019년 이후 전체적으로 물가 지수 추이가 매년 우상향을 보이고 있다. <br/>
특히, 2020년 이후로는 소비자 물가 지수와 과일 물가 지수 증가율(%)이 매년 증가했고 <br/>
작년(2023년) 기준 가장 큰 증가율(**약 12%**)을 기록했다.

#### 채소 및 과일 품목별 물가 증가율 상위 5위 누적 빈도수 [2]
- 최근 9년간(2015년~2023년) 채소 및 과일 물가 상승 누적 상위 5개 품목 시각화

<p align="center">

  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/113625699/6a9dc61b-4f1f-4737-a34f-4f66efb04062" alt="Image 1" style="width:49%;">
  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/113625699/f8c6eadf-a7c6-4446-9b5c-3669ef101bfc" alt="Image 2" style="width:49%;">

</p>

- 채소별 상위 품목: **무, 감자, 당근, 배추, 양파** 등 
- 과일별 상위 품목: **귤, 사과, 수박, 감, 배** 등
  
#### 2023 분기별 농산물 물가 증감률 [1]
- 기준: 2020년(**100**)
- 예시: 2023년 1분기
<p align="center">
  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/163802905/f35dbf27-bb32-4d08-990c-5d45c3147d63" alt="Image 1" style="width:45%;">
</p>

- 분기별 농산물 물가 증감률 상위 2위 품목 
  * 1분기 : **당근**(52%), 양파(40%)
  * 2분기 : **양파**(34%), 당근(32%)
  * 3분기 : **사과**(37%), 귤(30%)
  * 4분기 : **사과**(62%), 복숭아(44%)
  
#### 국산 과일 가격 인상 시각화 [2]
- 해당연도: 2023 ~ 2024년
<p align="center">
  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/163802905/7534f4fe-ffbc-4c4e-8848-833d5f15411e" alt="Image 2" style="width:52%;">
</p>

- 해당연도: 2023년 vs 2024년 2월<br/>

 | |배|단감|사과|참다래(국내산 키위)|
|:------:|:---:|:---:|:---:|:---:|
|**2023년(원)**|26,943|11,902|22,956|9,049|
|**2024년 2월(원)**|41,379|21,505|29,259|10,263|
|**증감(원)**|+14,436|+9,603|+6,303|+1,214|


위 두 그래프를 통해 2023년 과실류 품목 중 **물가 및 가격 상승면**에서 **사과**가 상위품목에 속함을 확인했다. <br/>
이와 더불어 쉽게 접할 수 있는 **배, 단감** 등에 대한 가격도 인상됨을 확인했다. <br/>
이에 착안하여 과실류 물가 및 가격 변화가 **대체상품 구매** 등 새로운 구매 형태로의 영향을 소비자에게 끼쳤는지 분석하기 위해 <br/>
**물가 상승에 따른 과실 소비 시장**을 분석하였다. <br/>

#### 과실류 가격 증가가 소비자 구매에 끼친 영향력 분석
##### 생과일 vs 냉동과일(딸기), 생과일 vs 건조과일(사과) 수입 물량 추이 [3], [4], [5], [6]
- 해당연도: 2015~2023년
<p align="center">

  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/113625699/ce8154c9-5e1d-4b62-b6b3-1e02133584f7" alt="Image 1" style="width:55%;">
  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/113625699/24e10851-f9b0-4699-a09e-065744758cb6" alt="Image 2" style="width:35%;">

</p>

과실류 품목에 대한 소비 시장 분석을 최근 9년치 대체 과실(**건조 사과, 냉동 딸기**)수입 물량을 통해 간접적으로 분석했다. <br/>
- **생사과 vs 건조사과** 수입량 비교 결과
    - 2021년부터 생사과 수입제한
    - 동일연도 부터 건조사과 > 생 사과 수입 양상 지속
    - 작년(2023년) 건조 사과 최대 수입량 갱신(**약 8.8t**) 
- **생딸기 vs 냉동딸기** 수입량 비교 결과
    - 2019년부터 생딸기 수입제한
    - 동일연도부터 냉동 딸기 지속적 수입 증가(2021년: 약 9000t, 2022년: 약 12200t, 2023년: 약 12700t)
    - 작년(2023년) 냉동 딸기 최대 수입량 갱신(**약 12700t**)

### 🍐원인 도출🍐
- 생과일 수입 억제와 대조적인 냉동 및 건조 과일 수입 촉진으로 <br/>
과실류 소비 시장에서의의 **대체 과일 공급량 증가**를 확인할 수 있다. <br/>
- 하지만, 대체 과일 소비가 현 과일 값 문제에 대한 장기적인 해결책은 아니라고 판단했다. <br/> 
- **과일 값 폭등 현상**에 대한 이유로 **수요량을 따라가지 못하는 생산량 감소**를 내세웠다. <br/> 
- 조사 결과 생산량 감소의 원인으로 아래 2가지 근거가 뒷받침했다.
  - 1.**고령화 및 농가 인구 감소**
  - 2.**이상기후로 인한 재배면적 감소**

### 1. 고령화 및 농가 인구 감소
##### 연령별 인구수 통계 그래프[8]
- 해당연도: 1960 ~ 2024년
- 영유아부터 노년까지 인구수 조사

<p align="center">
  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/163129674/a1bf842e-57d9-4125-ba4a-9e53394e62c5" alt="Image 1" style="width:36%;">
</p>

- 1960년 이후 인구수는 지속적인 증가 추세를 보였다.<br/>
  - 1960년대(**약 2500만명**), 2020년대(**약 5000만명**)<br/>
- 그러나 시간 흐름에 따라 특정 연령별 인구수는 감소 추세를 보였다.<br/>
  - **영유아 ~ 청년층**은 1980년대 이후 지속적으로 감소했다.<br/>
  - 이와 대조적으로 **중년 ~ 노년층**은 동일기간 동안 증가했다.<br/>
  
##### 농가 인구수 감소와 65세 이상 고령인구비율 그래프 유사성[9], [10]
- 해당연도: 2013 ~ 2022년
- 행정구역 단위: 전국
  
<p align="center">
  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/163129674/1da46e5f-fd99-4259-b613-fd30f3cbf330" alt="Image 2" style="width:55%;">
</p>

- 전국 농가 인구수는 2010년대 이후 2022년까지 계속 감소 추세를 보였다.<br/>
  - 2022년 역대 최저 농가인구수 기록(**약 200만명**)<br/>
- 이와 대조적으로 동일기간 동안 인구비율에서 65세 이상이 차지하는 비중은 계속 증가 추세를 보였다.<br/>
  - 2022년 역대 최고 65세 이상 인구 비율 기록(**약 50%**)<br/>
- 특히 2020년 이후 **전국 농가 인구수가 가장 가파른 기울기로 감소**한 반면<br/>
  **인구비율에서 65세 이상 비중은 가장 가파른 기울기로 증가**했다.<br/>
- 이를 통해, 최근 전국 농가 인구수 변화와 전체 인구 비율에서의 65세 비중 변화간의 유사성이 있음을 관찰할 수 있다.

#### 1차 산업 숙련 종사자수 통계[11]
- 해당연도: 2004 ~ 2017년

<p align=center> 
  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/163129674/4ec810b3-bebc-4bcb-b36b-fa5f586df9fc" alt="appleNews" style="width:55%;">
</p> 

- 최근 10년간 1차 산업 숙련 종사자 수가 감소 추세를 보였다.<br/>
  - **숙련 종사자**: 전문적 기술이 필요한 직무 종사자<br/>
- 2004년 **약 1800명**인 농업 관련 1차 산업 종사자 수는 2017년 **약 1200명**으로 감소했는데<br/>
마지막 집계시점이 2017년 인것을 고려하면 더 감소할 것으로 예상된다.<br/>

### 2. 이상기후로 인한 재배면적 감소
#### 권역별 논밭 경지면적 변화[12]
- 해당연도: 2014 ~ 2023년
- 행정구역 단위: 전국

<p align="center">
  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/108911726/890e1529-7cc8-4b50-a101-ad2468989df5" alt="Image 1" style="width:32%;">
</p>

- 최근 10년간 권역별 논밭 경지면적은 하락세를 보였다.<br/>
  - 2023년 기준 **경상권,호남권,충청권**에서 가장 큰 하락세를 보였다.<br/>

#### 23년도 가격 증감률이 높은 품목 3종류의 재배면적 비교[],[],[]
- 해당연도: 1990 ~ 2023년
- 행정구역 단위: 전국
<p align="center">
    <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/108911726/8c578c05-2b0e-44e7-bb6d-103aade17e1b" alt="pear" style="width:32%;">
</p>
- **배**는 2000년 이후로 전국적 **하락세**를 보였다.<br/>

<p align="center">
    <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/108911726/7b17a64d-f15c-4360-90a5-b9623db7ecb1" alt="apple" style="width:32%;">
</p>

- **사과**는 2020년 이후로 남부(**경상권**)은 **하락세**, 북부(**강원권**)은 **상승세**를 보였다.<br/>
    - 단위면적당 재배 농지의 **최대 하락세**는 **경상권**이다.<br/>

<p align="center">
    <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/108911726/dd7712df-31eb-4077-8124-a3b2ee422ce6" alt="onion" style="width:32%;">
</p>

- **양파**는 2020년 이후로 남부(**호남권&경상권**)은 **하락세**, 북부(**수도권&강원권**)은 **상승세**를 보였다.<br/>


#### 사과 & 양파 재배면적의 변화율 분석[],[]
- 해당연도: 사과(1990 ~ 2023년), 양파(2010 ~ 2023년) 
- 행정구역 단위: 사과(강원권&경상권), 양파(수도권&강원권)

<p align="center">

  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/108911726/29644ffe-e0f1-412c-9d46-8c4d681749de" alt="Image 1" style="width:49%;">
  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/108911726/e6f52c1f-b11b-4f52-bdea-01a0b87704bb" alt="Image 1" style="width:47%;">

</p>

- 사과 및 양파의 재배면적이 남부 권역에 비해 북부 권역이 **상승세**를 보였다.<br/>
  - 재배지역의 '**북상**'을 확인<br/>

- 재배지역 **북상**의 원인으로 **연평균 기온 상승**이 있음을 예상했다.<br/>


#### 농산물 재배 지역의 북상 : 연평균 기온 상승 및 시계열 예측[],[]
- 해당연도: 1980 ~ 2023년
- 행정구역 단위: 전국
<p align="center">

  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/108911726/63582075-cbd1-475f-b08b-85710fbc4464" alt="Image 1" style="width:48%;">
  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/108911726/ee8f64cb-4468-4576-8bbb-4ac93f9eb2ed" alt="Image 1" style="width:51%;">

</p>

- 1980년 이후부터 연평균 기온은 **상승세**를 보였다.<br/>
  - 2023년에 최대치 기록(13.9도)<br/>

- 1905년부터 118개의 연평균 기온 데이터를 토대로 시계열 예측한 결과, **지속적인 기온 상승**을 보였다.<br/>


#### 분석 결과
→ 고령화 및 농가 인구 감소는 노동력 감소를 나타내고,
    이상기후로 인한 재배면적 감소는 직접적인 생산량 감소를 나타낸다.<br/>

### 💡해결책 제시💡
#### 스마트팜
- 앞서 분석한 **농업 노동력 감소 및 재배면적 감소**에 대한 해결책들 중 하나로 **스마트팜**을 제시한다.<br/>
- 이는 **시간과 공간의 무제약**을 원칙으로 정보통신기술(ICT)을 활용해 작물의 생육환경을 관측하고 최적의 상태로 관리하는 과학 기반의 농업방식이다.
- 또한, 빅데이터 기술과 결합해 최적화된 생육환경 제공, 수확량 예측 등 생산 및 관리 시스템에서 최적화된 의사결정을 가능하게 한다. 
- 현재는 스마트팜 도입 초기 단계로 정부에서 2019년 이후부터 적극적으로 권장하며, 이를 통해 **노동시간 감소 및 농산물 생산량 증가** 등을 목표로 한다.


#### 스마트팜 제시 근거 [16] [17]
##### 1. 구글 트랜드 분석 통한 관심도 변화
- 해당연도: 2021년 12월 1일~2024년 3월 21일
 
<p align="center">
  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/113625699/dbb74260-62a7-494a-be47-789b11896893" alt="Image 1" style="width:45%;">
</p>

구글 트랜드 분석을 통해 웹상에서 **'스마트팜'** 단어에 대한 관심도를 관측할 수 있다. <br/>
'스마트팜' 단어 월별 검색 횟수 상위 5개를 살펴본 결과, **2022년 이후** 높은 관심을 보임을 알 수 있다. <br/>
- 2022년 5월(**448회**), 2023년 4월(**404회**), 2022년 10월(**399회**), 2022년 7월(**365회**), 2023년 3월(**346회**) <br/>

~~→ 농산물 생산성 증대의 해법으로 스마트팜을 솔루션으로 채택하는 수요가 증가함으로 해석  
→ 농림축산식품부에서 스마트팜을 **정량평가 대상**으로 지정함을 확인~~
##### 2-1. 스마트팜 효용성 정량평가 결과(1)- 농작물 생산량
- 집계연도: 2020~2021년
- 생산량 단위면적당 생산량(kg/3.3m^2)
  
<p align="center">
  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/70615068/209df21e-4ae3-4b8f-a9ae-06348246e4ca" alt="Image 1" style="width:25%;">
</p>

- 스마트팜 운영에 따른 연차별 농작물 생산량이 스마트팜 도입 이후 증가했다. <br/>
- 특히, 3년차인 2021년에 **최대 11.55%** 증가했다.

##### 2-2. 스마트팜 효용성 정량평가 결과(2)- 농업소득
- 집계연도: 2020~2021년
- 생산량 단위면적당 생산량(x만원/3.3m^2)
  
<p align="center">
  <img src="https://github.com/addinedu-ros-5th/eda-repo-2/assets/70615068/dfd95f98-a5e3-4125-9dbc-f49154889da7" alt="Image 2" style="width:25%;">
</p>

- 스마트팜 운영에 따른 연차별 순이익이 스마트팜 도입 이후 증가했다. <br/>
- 특히 2021년에 **신규 스마트팜 농가 증가률**이 **최대 47.31%** 이르렀다. <br/>
  
### 💡결론💡
- 소비자 물가 지수 상승과 견주어 최근 과일값 폭등에 대해 분석 결과 <br/>
전반적인 수요량 대비 **공급량 감소**가 원인이었다.
- 이는 **고령화 및 농가 인구 감소, 이상기후로 인한 재배면적 감소**가 주된 원인이 되었다.
- 전국 농가 인구층에서 **65세 이상**이 높은 비중을 차지했고 **농업 관련 숙련 종사자 수 감소**를 확인했다.
- 또한, 연평균 기온 변화 분석 결과 재배면적의 감소와 북상으로 인한 **재배적지 감소**를 확인했다. 
- 위 문제들의 해결방안들 중 하나로 **스마트팜**을 잠재적인 솔루션으로 채택했고 그에 대한 수요가 증가하고 있음을 확인했다.
- 특히, 농림축산식품부에서는 스마트팜을 **정량평가 대상**으로 지정하고 관련된 제도 및 프로그램을 통해 농산물 생산성 증대를 목표로 하고 있다.
- 따라서, 스마트팜에 대한 제도적 확산과 구제적인 교육 프로그램 수립을 통한 과학 기반의 농업이 **노동 시간 감소와 생산량 증대**를 이끌 것으로 전망된다.  
~~→ 농산물 생산성 증대의 해법으로 스마트팜을 솔루션으로 채택하는 수요가 증가함으로 해석  
→ 농림축산식품부에서 스마트팜을 **정량평가 대상**으로 지정함을 확인~~

### 출처
- 1: [품목별 소비자물가지수-통계청, 품목별 및 시점 설정: 총지수, (농산물)채소, (농산물)과실 (2014~2023)](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1J22112&conn_path=I2)

- 2: [소매가격-농산물유통정보](https://www.kamis.or.kr/customer/main/main.do)

- 3:[한국무역통계진흥원,생딸기, 검색순서:과실·견과류→0810→081010→[0810100000]](https://www.bandtrass.or.kr/customs/total.do?command=CUS001View&viewCode=CUS00201)

- 4:[한국무역통계진흥원, 냉동딸기, 검색순서: 과실·견과류→0811→081110→[0811100000]](https://www.bandtrass.or.kr/customs/total.do?command=CUS001View&viewCode=CUS00201)

- 5: [한국무역통계진흥원, 생사과, 검색순서:과실·견과류→0808→080810→[0808100000]](https://www.bandtrass.or.kr/customs/total.do?command=CUS001View&viewCode=CUS00201)

- 6: [한국무역통계진흥원,  건조사과, 검색순서:과실·견과류→0813→081330→[0813300000]](https://www.bandtrass.or.kr/customs/total.do?command=CUS001View&viewCode=CUS00201)


- 7: [통계청. 『채소생산량(과채류)』](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1ET0027&vw_cd=MT_ZTITLE&[…]th=MT_ZTITLE&path=%252FstatisticsList%252FstatisticsListIndex.do)

- 8: [통계청. 『[장래인구]성 및 연령별 추계인구/전국) 1960-2023』](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1BPA001&vw_cd=MT_ZTITLE&[…]th=MT_ZTITLE&path=%252FstatisticsList%252FstatisticsListIndex.do)

- 9: [통계청. 『고령인구비율(시도/시/군/구) 2000-2023』](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1YL20631&conn_path=I2) 

- 10: [통계청. 『[농가인구수]행정구역별 농가인구』](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1EA1011&vw_cd=MT_ZTITLE&[…]th=MT_ZTITLE&path=%252FstatisticsList%252FstatisticsListIndex.do)

- 11: [통계청. 『1차 산업숙련 종사자수』](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1DA7C08S&vw_cd=MT_ZTITLE&list_id=B17A&scrId=&seqNo=&lang_mode=ko&obj_var_id=&itm_id=&conn_path=MT_ZTITLE&path=%252FstatisticsList%252FstatisticsListIndex.do)

- 12: [통계청.『전국(도별) 논밭별 경지면적』](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1EB001&conn_path=I2)

- 13: [기상청.『전국 기후변화 시나리오』](http://www.climate.go.kr/home/CCS/regionclimate/main_view.html)

- 14: [기상청 날씨누리.『과거관측-일별자료-』](https://www.weather.go.kr/w/obs-climate/land/past-obs/obs-by-day.do?stn=108&yy=2005&mm=3&obs=1)

-  15: [스마트팜 구글 트랜드 분석](https://trends.google.com/trends/explore?date=2020-02-20%202024-03-20&geo=KR&q=%EC%8A%A4%EB%A7%88%ED%8A%B8%ED%8C%9C)

- 16: [농림축산식품부.(2023). ***『스마트농업 실태조사』*** n.p.: 농림축산식품부. pp121-122](https://www.smartfarmkorea.net/file/download.do;jsessionid=AK3Mg84InUsxoe9loLVYtG4Dsi1LPJh9DsX7YRkkCdLy1wVazSOSFqg2ag3I8a2s.ICTfusionwas2_servlet_smffront?fileId=3365&type=BBS)
