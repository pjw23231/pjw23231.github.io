---
title: "CIFAR-10 Image Classification"
excerpt: "딥러닝 기반 이미지 분류 및 모델 성능 최적화"
collection: portfolio
permalink: /portfolio/cifar10/
---

## 1. Project Overview

CIFAR-10 데이터셋을 활용하여 이미지 분류 모델을
학습하고 다양한 성능 개선 전략을 탐구하였다.

MNIST보다 복잡한 컬러 이미지 데이터를 활용하여
모델의 특징 추출 능력과 일반화 성능을 분석하였다.

## 2. Project Objective

- 이미지 분류 모델 구현
- 다양한 신경망 구조 비교
- 데이터 증강을 통한 일반화 성능 개선
- 모델의 예측 정확도 최적화

## 3. Dataset

| Category | Description |
| --- | --- |
| Dataset | CIFAR-10 |
| Total Images | 60,000 |
| Training Images | 50,000 |
| Test Images | 10,000 |
| Image Size | 32 x 32 |
| Channels | RGB |
| Classes | 10 |

### Classification Categories

- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck

## 4. Technologies

- Python
- PyTorch
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Kaggle

## 5. Model Architecture

이미지 특징 추출 및 분류 성능 개선을 위해
다양한 딥러닝 모델 구조를 검토하였다.

### Candidate Models

- Convolutional Neural Network (CNN)
- ResNet
- ConvNeXt
- Vision Transformer (ViT)

## 6. Optimization Strategy

| Method | Purpose |
| --- | --- |
| Data Augmentation | 데이터 다양성 확보 |
| Architecture Selection | 특징 추출 능력 개선 |
| Hyperparameter Tuning | 학습 조건 최적화 |
| Model Evaluation | 일반화 성능 검증 |

## 7. Results

이미지 분류 모델의 학습 및 성능 개선 실험을 수행하였다.

세부 모델별 실험 결과와 최종 Kaggle 점수는
실험 기록을 정리한 후 추가할 예정이다.

## 8. Key Takeaways

- 컬러 이미지의 특징 추출 방법을 학습하였다.
- 이미지 분류 모델의 구조적 차이를 이해하였다.
- 데이터 증강과 모델 최적화 방법을 탐구하였다.
- 모델의 정확도와 일반화 성능을 분석하였다.

## 9. Future Improvements

- 모델별 정확도 비교
- 학습 시간 및 연산 비용 비교
- Confusion Matrix 시각화
- 오분류 이미지 분석
- 모델 앙상블 실험
