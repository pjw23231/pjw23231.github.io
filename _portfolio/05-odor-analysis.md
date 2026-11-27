---
title: Odor Complaint Data Analysis
excerpt: 전주 악취 민원 텍스트 전처리 및 데이터 분석
collection: portfolio
permalink: /portfolio/odor-analysis/
---

## 1. Project Overview

악취 민원 데이터를 활용하여 비정형 텍스트를 구조화하고 민원의 유형과 공간적 특성을 분석하는 프로젝트이다.

## 2. Problem Definition

민원 내용은 자유롭게 작성된 문장으로 구성되어 있어 유형별 비교와 지역별 현황 파악이 어렵다.

## 3. Dataset

| 항목 | 내용 |
| --- | --- |
| 일시 | 민원 발생 시점 |
| 위치 | 발생 지역 |
| 내용 | 민원 텍스트 |
| 결과 | 처리 결과 |
| Lat / Lon | 공간 분석용 좌표 |
| 세부분류 | 민원 유형 |

## 4. Methodology

- 결측치 및 텍스트 정제
- P0~P4 단계별 전처리 실험
- 형태소 분석 및 TF-IDF 기반 특징 추출 검토
- 민원 유형별 분류와 시공간 시각화 설계

## 5. Evaluation Plan

분류 실험에서는 Precision, Recall, F1-score 및 Confusion Matrix를 활용할 계획이다. 공간 분석에서는 위치 정보의 정확성과 개인정보 보호를 고려한다.

## 6. Current Status

데이터 구조 및 전처리 과정을 정리하였다. 최종 분류 성능과 지도 분석 결과는 검증 후 추가할 예정이다.

## 7. Future Improvements

- 유형별 데이터 불균형 분석
- 민원 발생 패턴 시각화
- 비식별화된 데이터와 재현 가능한 분석 코드 정리
