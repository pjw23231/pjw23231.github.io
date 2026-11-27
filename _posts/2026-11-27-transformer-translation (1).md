---
title: Transformer — 번역 능력은 어떻게 학습될까?
date: 2026-11-27 00:00:00 +0900
permalink: /posts/transformer-translation/
categories:
- Natural Language Processing
tags:
- Natural Language Processing
excerpt: Encoder와 Decoder, teacher forcing, causal mask의 역할을 정리한다.
---

## 문제 정의
원문 전체를 이해하면서 번역문을 순차적으로 생성해야 한다.

## 핵심 원리
Encoder는 원문 토큰의 문맥 표현을 만든다. Decoder는 이전 번역 토큰과 Encoder 출력을 이용해 다음 토큰의 확률을 예측한다. 학습 중에는 정답을 한 칸 이동하여 입력과 목표를 구성하고 causal mask로 미래 토큰 접근을 차단한다.

## 구현 예제: 인과 마스크
```python
import torch
n = 4
mask = torch.triu(torch.ones(n,n,dtype=torch.bool), diagonal=1)
print(mask)
```

이 마스크는 PyTorch MultiheadAttention의 boolean attn_mask에서 True 위치를 차단하는 방식과 맞는다. 다른 API는 의미가 다를 수 있다.

## 분석
Cross-entropy로 정답 토큰의 확률을 높인다. 추론 시에는 이전에 생성한 토큰을 입력으로 사용하므로 학습과 추론 조건에 차이가 있다.

## 다음 실험
토큰화, 패딩 마스크, 번역 평가 지표를 포함한 작은 번역 실험을 구성한다.
