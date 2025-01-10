# first-repository
add new contents

diabetes.py : 당뇨병 데이터에 대해서 모델을 직접 작성 후 플롯까지.  
bike_sharing.py : 자전거 대여 데이터에 대해서 사이킷런 선형회귀를 통한 분석 후 플롯까지.

# 당뇨병 데이터셋 회귀분석
이 프로젝트는 당뇨병 데이터셋을 활용해 회귀 모델을 학습시키고 평가하며, 이 때 모델은 직접 구현한 Gradient Descent을 활용한 선형 회귀로 주어집니다.

## 모델링
1. 선형회귀 모델 구현
2. loss function으로 MSE를 채택하였고, loss function에 대한 analytic 미분을 통해 경사하강법을 구현하였음

## 평가
1. evaluation metric으로 동일하게 MSE를 채택하여 모델 성능 평가
2. 실제값과 예측값에 대한 시각화


# Bike Sharing Demand 분석 / 예측
이 프로젝트는 Bike Sharing Demand 데이터를 활용해 자전거 대여 수요를 예측하는 작업을 다룹니다.
데이터의 간단한 전처리, EDA, 모델링 과정을 통해 기본적인 선형회귀 모델을 구현했습니다.

## 데이터 로드 및 전처리
1. datetime 데이터를 연, 월, 일, 시, 분, 초로 분리하여 분석 가능하도록 변환.
2. min과 sec 데이터는 모두 0으로 동일하므로 제거.
3. temp와 atemp의 높은 상관관계를 고려해 atemp를 제거.
4. 나머지 유의미한 특성(season, holiday, workingday, 등)을 독립 변수로 사용.

## EDA
1. seaborn 활용하여 데이터 분포 시각화

## 모델 구성
1. 선형회귀 활용
2. 학습 데이터 훈련/테스트 용 분리
3. 평가지표로 MSE, RMSE 계산

## 시각화
1. temp, humidity에 대해서 scatterplot으로 실제/예측 데이터 간 비교 수행
