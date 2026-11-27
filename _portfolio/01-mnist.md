
---
title: "MNIST Image Classification"
excerpt: "CNN 기반 손글씨 숫자 분류 및 모델 성능 최적화"
collection: portfolio
permalink: /portfolio/mnist/
---

## 1. Project Overview

MNIST 데이터셋을 활용하여 손글씨 숫자 이미지를
분류하는 딥러닝 모델을 개발하고 성능을 개선하였다.

## 2. Project Objective

- CNN 기반 이미지 분류 모델 구현
- 데이터 증강을 통한 일반화 성능 개선
- 모델 구조 및 학습 전략 최적화
- Kaggle 분류 정확도 향상

## 3. Dataset

| Category | Description |
| --- | --- |
| Dataset | MNIST |
| Image Size | 28 x 28 |
| Channels | Grayscale |
| Classes | 10 (0-9) |
| Task | Image Classification |

## 4. Technologies

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Kaggle

## 5. Model Architecture

CNN을 기반으로 이미지의 공간적 특징을 추출하고,
Global Average Pooling을 활용하여 최종 분류를 수행하였다.

```text
Input Image
    |
Convolution Layer 1
    |
Convolution Layer 2
    |
Convolution Layer 3
    |
Convolution Layer 4
    |
Global Average Pooling
    |
Dense (10 Classes)
    |
Prediction
```

## 6. Optimization Strategy

| Method | Purpose |
| --- | --- |
| Data Augmentation | 일반화 성능 개선 |
| Global Average Pooling | 파라미터 감소 |
| Early Stopping | 과적합 방지 |
| Learning Rate Scheduling | 안정적인 모델 최적화 |

## 7. Results

| Evaluation Metric | Result |
| --- | --- |
| Kaggle Accuracy | 0.99675 |
| Accuracy (%) | 99.675% |

**Best Kaggle Score: 99.675%**

## 8. Key Takeaways

- CNN을 활용한 이미지 특징 추출 방법을 학습하였다.
- 데이터 증강과 모델 구조를 활용한 성능 개선을 실험하였다.
- 학습률 조절과 과적합 방지 기법을 적용하였다.
- 모델 성능을 평가하고 개선하는 과정을 경험하였다.

## 9. Future Improvements

- 다양한 CNN 아키텍처 비교
- 오분류 이미지 분석
- 모델별 성능 및 학습 시간 비교
- 실험 결과 시각화
