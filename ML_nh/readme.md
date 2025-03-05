### 사용한 데이터
- Data domain : 의료/bio 관련 데이터
- 데이터 사이즈는 500개부터 20만개까지 다양함.
- 예측 변수 (y)는 모두 이진 변수로, 분류 문제
- 데이터 링크: \
  Thyroid Cancer Risk (212691 x 17): https://www.kaggle.com/datasets/mzohaibzeeshan/thyroid-cancer-risk-dataset 

  Alzheimer (74283 × 25): https://www.kaggle.com/datasets/ankushpanday1/alzheimers-prediction-dataset-global
  
  Breast Cancer Prediction (4024 × 16): https://www.kaggle.com/datasets/reihanenamdari/breast-cancer 

  Heart Failure prediction (918 × 12): https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction 

  Heart Disease (303 x 14) https://www.kaggle.com/datasets/yasserh/heart-disease-dataset?select=heart.csv

### 사용한 주요 머신러닝 모델
1. Logistic Regression
2. Random Forest
3. Decision Tree
4. LightGBM
5. XGBoost
6. CatBosot

데이터 분할: train 8 test 2 \
feature selection: 데이터셋의 피처 중 '유의미한 피처'만 뽑아서 학습하는 과정을 거침 (t-test와 카이제곱 검정으로 각 변수의 p-value를 확인해서 판단함)\
Hyperparameter: 머신러닝 모델 중 boosting 모델은 전부 optuna를 활용한 하이퍼파라미터 최적화 진행함. (Lightgbm, xgboost, catboost)
   
### 남은 할 일
- thyroid cancer risk dataset 분할해서 학습시켜보기. (1k 이하, 5k, 10k, 15k 순서대로)
- 분석 방향성 브레인스토밍: 가장 성능이 좋은 딥러닝 모델이 하나로 수렴하는지? -> 수렴한다면, 그 딥러닝 모델이 다른 모델들과 갖는 결정적인 차이점이 있는지?
- ML에 가장 잘 작동하는 데이터셋 사이즈가 정해져 있을까? (303rows를 가지고 있는 heart disease dataset은 다른 데이터에 비해 유의미한 피처도 많았지만 정확도가 낮았음.)  -> 데이터셋 사이즈와 관련된 논문이 있는지 찾아보기
