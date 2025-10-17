# ⚽ Football Shots Classification Project

> **기간:** 2025.10.15 ~ 2025.10.17  
> **데이터 출처:** [Kaggle - Football Database](https://www.kaggle.com/datasets/technika148/football-database?select=shots.csv)  
> **사용 툴:** Orange3  
> **발표 자료 & Orange Workflow:** [Football Shots 예측 모델 분석](https://github.com/pythoncide/Orange3/blob/main/Football_Shots_Prediction_Model_Analysis.pdf)

---

## 🧭 프로젝트 개요
유럽 5대 리그 경기의 **슛 데이터(`shots.csv`)** 를 활용하여  
경기 중 발생한 슛을 **위치와 상황 정보에 따라 분류(Classification)** 하는 모델을 구축하였습니다.

- **슛 타입 분류:** Head / Foot / OtherBodyPart  
- **골 여부 분류:** Goal / NoGoal  

---

## 🧩 분석 구성
1. **슛 위치 기반 슛 타입 분류 모델**  
   - 사용 모델: Logistic Regression / Random Forest / AdaBoost  
   - 주요 변수: `positionX`, `positionY`, `lastAction`, `situation`

2. **슛 위치 기반 골 분류 모델**  
   - 사용 모델: kNN / Tree / Neural Network / Naive Bayes / Stack  
   - 불균형 데이터(골:노골 ≈ 1:9)에 따른 성능 비교 및 Threshold 실험

---

## 📊 결과 요약
- **슛 타입 분류 모델:** 약 **92% 정확도**, Random Forest가 가장 안정적인 성능  
- **골 분류 모델:** 정확도는 높았으나 불균형 데이터로 인한 Recall 저하  
- 공간적 변수(`positionX`, `positionY`)가 두 모델의 핵심 분류 요인으로 작용

---

## 🧠 향후 개선 방향
- 데이터 리샘플링(SMOTE) 및 Threshold 최적화 적용  
- xG(Expected Goal) 및 슈팅 각도·속도 변수 추가  
- 경기장 기반 시각화(Shot Map) 확장

---
