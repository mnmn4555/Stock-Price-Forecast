# Stock-Price-Forecast
## 코스피 주식 예측
> Library : LSTM, RNN, RandomForest, AdaBoost, LightGBM, scikit-learn, FinanceDataReader
> Environment : Google Colab
## Overview
* 주제 선정  
경제 상황, 금리, 주식 동향 등 주식 가격 결정에 영향을 미치는 요인은 다양하다. 하지만 이 모든 요인을 파악하고 주식 가격을 정확하게 예측하는 것에는 한계가 있다. 이를 위해 과거의 주식값의 흐름을 읽고 미래 주식값을 예측하는 방법으로 주식 가격을 예측하고자 한다.
  
* 분석 목표  
![image](https://user-images.githubusercontent.com/71176581/205050843-bd3ee73d-fb8f-469d-8dc9-6a95e6ea86b2.png)  
본 연구는 2019년 11월 1일부터 2022년 10월 31일까지 코스피 시가를 이용하여 다음날(2022년 11월 1일) 코스피 시가를 예측하는 것을 목표로 한다. 이를 위해 FinanaceDataReader 라이브러리에서 제공하는 코스피 시가를 이용한다.

* 2019-11-01 ~ 2022-10-31 코스피 시가 지수
![image](https://user-images.githubusercontent.com/71176581/205049894-89f33705-9f19-4a87-a523-b80842ce41bb.png)
위 그래프는 2019년 11월 1일부터 2022년 10월 31일까지 코스피 시가 데이터이다. 이 데이터의 후반부 150개를 test 데이터, 나머지는 train 데이터로 지정하여 학습한다.  
![image](https://user-images.githubusercontent.com/71176581/212311240-5ad8a581-5f2a-4f05-ad1c-aeeabf468d1d.png)  
데이터를 7일 단위로 나눠서 학습한 뒤, 다음날(2022년 11월 1일), 3일 뒤(2022년 11월 4일) 코스피 시가 지수를 예측한다.  
* 1일 뒤 RNN 예측결과   
![image](https://user-images.githubusercontent.com/71176581/205050073-d1299d96-09b4-4075-a03c-8c57d5144f37.png)  

* 1일 뒤 LSTM 예측결과  
![image](https://user-images.githubusercontent.com/71176581/205051479-1e201daf-d489-4045-a0bc-37b4b7d12256.png)  

* 1일 뒤 실제 코스피 시가 값과 예측한 코스피 시가 값 간 차이  
![image](https://user-images.githubusercontent.com/71176581/205052274-a819cee0-fd6f-4d0a-b520-6c612194bdb2.png)  

* 여러 알고리즘을 이용한 코스피 시가 예측  
> Grid Search  
> 알고리즘 별로 성능을 최적화하는 parameter을 선택하는 방법으로 같은 데이터라도 각 알고리즘 별 parameter 값이 다르다. 2019년 11월 01일 ~ 2022년 10월 31일 간 코스피 시가 데이터로 RandomForest, AdaBoost, XGBoost, LightGBM의 성능을 최적화하는 parameter를 알아본다.  

* 알고리즘별 최적 하이퍼파라미터 값
> RandomForest  
![image](https://user-images.githubusercontent.com/71176581/218246507-e44002b7-769f-42f3-88b1-e17b1f0ad089.png)  
> AdaBoost  
![image](https://user-images.githubusercontent.com/71176581/218246534-f907959e-85d5-416e-8bb9-39b78b9013e7.png)  
> XGBoost  
![image](https://user-images.githubusercontent.com/71176581/218246542-d18b151e-d228-4668-874f-d2f4a9a18455.png)  
> LightGBM  
![image](https://user-images.githubusercontent.com/71176581/218246547-651785ad-c7e5-4cfe-ac97-923530eef4ed.png)  

* RandomForest  
![image](https://user-images.githubusercontent.com/71176581/205057623-5c03089a-4bb1-40d8-b404-35537f58d241.png)
* AdaBoost  
![image](https://user-images.githubusercontent.com/71176581/205057752-a73dc33e-18f9-4e5e-86c0-99eab02cdd75.png)
* XGBoost  
![image](https://user-images.githubusercontent.com/71176581/205057767-f54340d2-f7b0-471b-bfe8-6675c57ade98.png)
* LightGBM  
![image](https://user-images.githubusercontent.com/71176581/205057808-54e31d16-252d-462f-9969-ac6ade00658c.png)  

* 1일 뒤 실제 코스피 시가 값과 예측한 코스피 시가 값  
![image](https://user-images.githubusercontent.com/71176581/218247079-d6be7bf0-192e-4b27-b432-722049af9f94.png)  

* 2022년 11월 1일 실제 코스피 시가와 예측한 코스피 시가의 RMSE 값  
![image](https://user-images.githubusercontent.com/71176581/218247113-15500bf5-08fc-4d38-a9e5-6baaa96dcb0e.png)  
