# IDS507_Midterm_Assignment

## 마감 
 5월 9일 2022년 11:59pm 블랙보드 제출

## 제출목록:
 1. 해당 과제에 쓰인 jupyter notebook(ipynb 파일)  (*주의사항 * a) 모든 줄에 주석 필수, 주석 없을 시 감점, b) 답이 명확하게 보일것. ) 
 2. jupyter notebook 의 모든 결과값을 출력하여 pdf로 변환 한 것(pdf 파일)

## 제출방법:
 위 두개의 파일(pdf, ipynb)파일을 블랙보드 중간고사과제칸에 제출하시면 됩니다.

## 데이터 설명 
본 과제에 사용된 데이터는 누수감지에 대한 데이터 이며 다음과 같은 컬럼을 가지고 있습니다.  

1. 누수감지 주파수 범위 
- LOW_HZ :: 10HZ 부터 240HZ 까지 
- HIGH_HZ :: 4000HZ 부터  4490HZ 까지 

2. 누수감지 횟수별 감지정보 
- max0 ~ max19 :  누수 감지 횟수 감지된 최대 주파수 HZ의 횟수 

3. 라벨
특정 누수타입에 대해 0과1로 라벨링 되어있습니다.

---
## 문제 

문제는 총 `10`문제 이며, 다음과 같습니다. 모든 문제는 서로 연관되어 있으니 연속하여 푸시길 바랍니다. 

### Q1. `data` 폴더에서 `train_data_1.csv`와 `train_data_2.csv`를 데이터프레임으로 불러온 후 두개의 데이터프레임을 병렬로 합쳐서 `df` 변수로 저장  
- 저장된 df 의 `형태` 출력 하기 (shape, 행과열 출력)
- 저장된 df 의 `컬럼 갯수` 출력하기( length of columns)

### Q2. df 데이터 프레임의 `LOW_HZ` 컬럼들에 대해 다음 출력하기 
- 각 컬럼의 `평균(mean)` 출력
- 각 컬럼의 `최대값(max)` 출력

### Q3. df 데이터 프레임 `max3` 컬럼의 유일값(unique)을 출력하고, max0~max19 컬럼 전체를 인코딩 하기

### Q4. df 데이터 프레임의 `80HZ` 컬럼 결측값의 합은 모두 얼마인가? 

### Q5. df 데이터 프레임의 결측치를 `interpolate`을 사용하여 행 단위로 채울고 (이때, 방법은 linear이며, 방향은 쌍방향) `40HZ` 컬럼의 합을 소수4번째 자리까지 구하기 

### Q6. df 데이터 프레임의 데이터를 X, 라벨(label)을 y로 할당 후 `train_test_split`함수를 사용하여 X_train, X_valid, y_train, y_valid 로 나누고, `X_train`을 기준으로 `X_train` 과 `X_valid` 의 `HIGH_HZ` 컬럼들을 `minmax scaler` 을 적용한 후 `x_valid`의 `4460HZ` 컬럼 `평균값`을 소수4번째 까지 구해 출력하기 
(이때, 테스트 비율은 0.2이고, random_state는 42로 고정 한다. minmax scaler의 최소값은 0, 최대값은 1로 설정)
(TIPS! 본 과제에는 test 데이터가 없으며, valid data만 있으므로 train : valid = 0.8 : 0.2 로 나누시면 되겠습니다.
또한,  min_max_scaler에 대해서는  scaler를 학습(fit) 시키고 변형(transform)을 해야되는데, 학습(fit)을 X_train으로 시키고, X_train과 X_valid를 변형(transform) 시키시면 됩니다. 

### Q7. `X_train` 의 **모든 변수** 와 `y_train` 을 사용하여 `LogisticRegression` 모델을 학습시키고, X_valid를 예측한후, y_valid와 모델의 결과값을 비교하여 정확도(Accuracy)를 출력하시오. 

### Q8. `모델의 예측값`과 `X_valid`에 대한 `혼돈 행렬(confusion matrix)` 그리고 `Roc-Auc` 값 출력 하기 

### Q9. `모델의 예측값`과 `X_valid`에 대한 `Roc curve`를 그리기

### Q10. 학습된 모델의 임계값(threshold)를 변형 해보고 그떄의 정확도(Accuracy)와 Roc-Auc score를 threshold와 같이 출력하시오.(단, [0.10, 0.22, 0.34, 0.46, 0.58, 0.70, 0.82, 0.94] 이다) 
