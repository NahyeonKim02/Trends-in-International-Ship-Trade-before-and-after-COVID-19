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
