---
title: Financial News Analysis & Visualization
excerpt: 금융 뉴스의 핵심 정보 추출과 의사결정 지원 시각화 (기획 중)
collection: portfolio
permalink: /portfolio/financial-nlp/
---

## 1. Project Overview

**Status: Planning**

금융 뉴스와 비정형 금융 정보를 자연어 처리 기술로 분석하고 사용자가 핵심 내용을 빠르게 이해할 수 있도록 시각화하는 프로젝트를 기획하고 있다.

## 2. Problem Definition

긴 뉴스 기사에는 기업, 경제 지표, 사건, 전망 등 다양한 정보가 혼재되어 있다. 핵심 사실과 해석을 구분하고 정보 간 관계를 직관적으로 표현하는 것이 목표이다.

## 3. Proposed Pipeline

```text
Financial News
    -> Text Preprocessing
    -> Entity / Event Extraction
    -> Summarization & Classification
    -> Information Visualization
```

## 4. Proposed Methods

- Transformer 기반 요약 및 정보 추출 검토
- 기업, 산업, 경제 지표 등 개체 추출
- 뉴스 주제 및 감성 분류 실험
- 필요 시 영어 뉴스의 한국어 번역
- 핵심 수치, 사건 관계 및 출처 시각화

## 5. Evaluation Plan

| 항목 | 평가 방향 |
| --- | --- |
| 정보 정확성 | 원문과 추출 결과 비교 |
| 요약 품질 | 핵심 정보 보존 및 사실 오류 검토 |
| 분류 성능 | 레이블 확보 후 F1-score 평가 |
| 사용자 경험 | 가독성과 핵심 정보 이해도 비교 |

## 6. Current Status

문제 정의 및 서비스 방향을 기획하는 단계이며 아직 검증된 모델 성능이나 투자 수익률은 없다.

## 7. Future Improvements

- 이용 조건이 확인된 뉴스 데이터 확보
- 기준 모델 구현 및 비교 실험
- 기사 출처와 사실·의견 구분 표시
- 사용자 중심 대시보드 구축

본 프로젝트는 금융 정보 이해를 돕는 학습 프로젝트이며 투자 수익이나 예측 정확도를 보장하지 않는다.
