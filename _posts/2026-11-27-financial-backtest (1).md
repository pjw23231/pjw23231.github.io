---
title: 금융 데이터 분석 — 수익률만으로 전략을 평가할 수 있을까?
date: 2026-11-27 00:00:00 +0900
permalink: /posts/financial-backtest/
categories:
- Financial Data Analysis
tags:
- Financial Data Analysis
excerpt: 누적 수익률과 최대 낙폭을 예시 데이터로 계산한다.
---

## 문제 정의
같은 수익률을 내더라도 손실 경로와 위험은 다를 수 있다.

## 핵심 원리
누적 수익률은 기간별 수익률을 복리로 연결한다. 최대 낙폭은 고점 대비 가장 큰 하락폭이다.

## 구현 예제
```python
import pandas as pd
r = pd.Series([0.05, -0.10, 0.08, 0.02])
wealth = pd.concat([pd.Series([1.]), (1+r).cumprod()], ignore_index=True)
drawdown = wealth / wealth.cummax() - 1
print('return:', wealth.iloc[-1]-1)
print('MDD:', drawdown.min())
```

## 분석
이 예시는 가상 수익률이며 실제 투자 성과가 아니다. 실제 백테스트에서는 거래 비용, 시점 일치, 미래 정보 누출, 생존 편향을 고려해야 한다.

## 다음 실험
동일 기간의 자산 배분 전략을 비교하고 수익률과 낙폭을 함께 기록한다.
