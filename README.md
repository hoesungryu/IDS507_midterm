# IDS507_Midterm_Assignment

## Q1. `data` 폴더에서 `train_data_1.csv`와 `train_data_2.csv`를 데이터프레임으로 불러온 후 두개의 데이터프레임을 병렬로 합쳐서 `df` 변수로 저장  
- 저장된 df 의 `형태` 출력 하기
- 저장된 df 의 `컬럼 갯수` 출력하기  

## Q2. df 데이터 프레임의 `LOW_HZ` 컬럼들에 대해 다음 출력하기 
- 각 컬럼의 `평균(mean)` 출력
- 각 컬럼의 `최대값(max)` 출력

## Q3. df 데이터 프레임의 `max3` 컬럼에 유일값(unique)은 무엇인가?

## Q4. df 데이터 프레임의 `80HZ` 컬럼 결측값의 합은 모두 얼마인가? 

## Q5. df 데이터 프레임의 결측치를 `interpolate`을 사용하여 행 단위로 채울고 (이때, 방법은 linear이며, 방향은 쌍방향) `40HZ` 컬럼의 합을 소수4번째 자리까지 구하기 

## Q6. df 데이터 프레임의 `HIGH_HZ` 컬럼들을 `minmax scaler` 을 적용한 후 `4460HZ` 컬럼의 `평균값`을 소수4번째 까지 구해 출력하기 (min=0, max=1)

## Q7. df 데이터 프레임의 데이터를 X, 라벨을 y로 할당 후 `train_test_split`함수를 사용하여 X_train, X_valid, y_train, y_valid 로 나누기 (이때, test_size=0.2 ,stratify=y, random_state = 42 로 설정) 그 다음 `LogisticRegression` 모델을 학습시키고, X_valid를 예측한후, `threholds [0.3 , 0.33 ,0.36,0.39, 0.42 , 0.45 ,0.48, 0.50]` 에 대하여 각각 정확도(Accuracy) 출력하기 

## Q8. `모델의 예측값`과 `X_valid`에 대한 `혼돈 행렬(confusion matrix)`그리기

## Q9. `모델의 예측값`과 `X_valid`에 대한 `Roc curve`를 그리고 `Roc-Auc` 출력 하기 


