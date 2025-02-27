### 사용한 데이터
- Data domain : 의료/bio 관련 데이터
- 데이터 사이즈는 500개부터 20만개까지 다양함.
- 예측 변수 (y)는 모두 이진 변수로, 분류 문제

### 사용한 주요 머신러닝 모델
1. Logistic Regression
2. Random Forest
3. Decision Tree
4. LightGBM
5. XGBoost
6. CatBosot

데이터 분할: train 8 test 2
머신러닝 모델 중 boosting 모델은 전부 optuna를 활용한 하이퍼파라미터 최적화 진행함. (Lightgbm, xgboost, catboost)
   
