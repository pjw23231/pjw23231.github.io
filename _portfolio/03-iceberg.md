---
title: Statoil/C-CORE Iceberg Classification
excerpt: SAR 이미지 분류 — Private Log Loss 0.07436
collection: portfolio
permalink: /portfolio/iceberg/
---

## 1. Project Overview

Kaggle의 Statoil/C-CORE Iceberg Classifier Challenge에서 위성 레이더 데이터를 활용하여 빙산과 선박을 구분하는 이진 분류 모델을 실험하였다.

## 2. Problem Definition

레이더 이미지의 형태와 반사 특성을 학습하여 빙산일 확률을 예측한다. 정확도뿐 아니라 예측 확률의 품질을 평가하는 Log Loss를 개선하는 것이 목표이다.

## 3. Dataset

- 75 × 75 크기의 두 레이더 밴드
- 입사각(inc_angle) 정보
- 이진 분류 레이블

## 4. Methodology

| 방법 | 목적 |
| --- | --- |
| SimpleCNN | 이미지 특징 추출 |
| 8방향 TTA | 변환된 이미지 예측의 통합 |
| Pseudo-labeling | 비라벨 데이터 활용 실험 |
| Stacking | 모델 예측과 이미지 통계, 입사각 정보 결합 실험 |

## 5. Results

| 지표 | 결과 |
| --- | --- |
| Private Leaderboard Log Loss | **0.07436** |

목표였던 0.10 미만의 Log Loss를 달성하였다. 개별 기법의 기여도는 추가 실험 기록을 통해 검증할 예정이다.

## 6. Future Improvements

- Pseudo-label 신뢰도 및 오류 전파 분석
- 확률 보정과 교차 검증
- 기법별 제거 실험 및 재현 코드 정리

[Competition](https://www.kaggle.com/c/statoil-iceberg-classifier-challenge)
