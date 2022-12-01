# Stock-Price-Forecast
## 코스피 주식 예측
> Library : LSTM, RNN, RandomForest, AdaBoost, LightGBM, scikit-learn  
> Environment : Google Colab
## Overview
* 주제 선정
한국 주식 가격, 미국주식 가격, 지수, 환율, 암호화폐 가격 등 금융 데이터 수집 라이브러리인 FinanceDataReader을 이용하여 과거 코스피 지수를 이용하여 다음날 코스피 지수 시가를 예측하고자 한다.
* 사용한 데이터
2019-11-1 ~ 2022-10-31 3년간의 코스피 시가 지수를 이용한다.
* 2019-11-1 ~ 2022-10-31 코스피 시가 지수
![image](https://user-images.githubusercontent.com/71176581/205049894-89f33705-9f19-4a87-a523-b80842ce41bb.png)

* 1일 뒤 예측
![image](https://user-images.githubusercontent.com/71176581/205050843-bd3ee73d-fb8f-469d-8dc9-6a95e6ea86b2.png)

* 1일 뒤 RNN 예측결과 (filter 14, filter 30)
![image](https://user-images.githubusercontent.com/71176581/205050073-d1299d96-09b4-4075-a03c-8c57d5144f37.png)  
![image](https://user-images.githubusercontent.com/71176581/205051347-11b1c23d-9dbf-47b8-a2c9-498d8aafba8a.png)

* 1일 뒤 LSTM 예측결과 (filter 14, filter 30)
![image](https://user-images.githubusercontent.com/71176581/205051479-1e201daf-d489-4045-a0bc-37b4b7d12256.png)
![image](https://user-images.githubusercontent.com/71176581/205051494-3ac72efd-6f88-4f61-9d2b-7c1b045f2ff8.png)
