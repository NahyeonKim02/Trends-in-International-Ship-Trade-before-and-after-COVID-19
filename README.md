# 📌 COVID-19 전후에 따른 국제선박무역 추이

### ⭐ 코드의 목적
의사결정나무(Decision Tree)와 랜덤포레스트(Random Forest) 모델의 성능을 비교합니다.
데이터를 효과적으로 분리 및 평가하여 최적의 학습 모델을 선정합니다.

모든 변수를 사용한 학습한 결과, 10개 속성만 선택 후 사용한 학습 결과를 포함하고 있습니다.

---

### ✨ 주요 내용

- SMOTE를 이용한 데이터 불균형 문제 해결
- 데이터 분할 (Train / Test)
- 학습 모델 성능 평가 (Accuracy, Precision, Recall, F1-Score)
- 교차 검증 (Cross Validation)
- 학습 곡선 시각화 (Learning curve)
- 분산 분석 (ANOVA)
- 새로운 데이터 예측

---

### 👨‍💻 예측 모델 만들기

- 실질적인 예측 데이터를 활용하기 위해 Random Forest 예측 모델을 생성하였습니다.
- ```rt_model.predict(X_ohe_new_adj)``` 코드를 통해 예측값을 도출했습니다.
- 범주형 데이터(```room_type_reserved```, ```market_segment_type``` 등)를 머신러닝 모델이 처리할 수 있도록, 숫자 데이터로 변환하기 위해 One-hot-encoding을 적용하였습니다.

---

### 💻 사용 Tool
- Python (Jupyter Notebook)
- Excel

---

### 📂 사용된 라이브러리
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Imbalanced-learn

---

### 🗂️ 데이터 설명

- **Dataset**: [hotel reservation_original.csv](https://www.kaggle.com/datasets/ahsan81/hotel-reservations-classification-dataset)
- **Target Column**: ```booking_status```

---

### 📊 주요 결과

- 랜덤포레스트(Random Forest)가 의사결정나무(Decision Tree)보다 성능이 우수합니다.
- 정확도와 추가적인 성능 지표(Precision, Recall, F1-Score)는 결과 섹션도 함께 출력합니다.
- 학습 곡선 분석 결과, 랜덤포레스트는 더 안정적이고 일반화 능력이 뛰어난 모델임을 확인할 수 있습니다.
- ANOVA 분석을 통해 모델의 평균 성능도 검증 완료하였습니다.

- 2020~2021년 동안 전반적인 입출항횟수가 가장 많았던 항구는 부산항이었다. 인천항, 울산항이 그 뒤를 이었다.
- 코로나로 인한 국제무역 둔화를 예상했던 것과는 다르게, 2020년과 2021년의 입출항횟수는 약 -3%의 감소를 보이며 큰 차이가 나타나지 않았다. 각 연도의 입항과 출항도 크게 다르지 않았다.
- 입출에 따른 총톤수도 비슷한 통계값을 나타내었다.
- 입항인 경우의 선박유형 비율과 출항인 경우의 선박유형 비율 또한 둘다 풀컨테이너선, 국제카페리, 여객선 순으로 상당히 유사하였다.
- 마지막으로 입출항횟수와 총톤수는 완벽한 양의 관계를 나타내진 않았다. 첫번째로 살펴보았던 항명과 입출항횟수의 관계를 항명과 총톤수로 변경하였을 때, 부산>인천>울산 순에서 부산>울산>광양 순으로 결과값이 다른 모습을 보였다.
