---
title: Self-Attention — 단어 사이의 관계는 어떻게 계산할까?
date: 2026-11-27 00:00:00 +0900
permalink: /posts/self-attention/
categories:
- Natural Language Processing
tags:
- Natural Language Processing
excerpt: Query, Key, Value와 scaled dot-product attention을 이해한다.
---

## 문제 정의
같은 단어도 주변 문맥에 따라 의미가 달라진다. 각 토큰이 다른 토큰의 정보를 선택적으로 활용할 방법이 필요하다.

## 핵심 원리
Query와 Key의 내적을 키 차원의 제곱근으로 나눈 뒤 softmax로 가중치를 계산한다. 이 가중치를 Value에 곱해 문맥 정보를 모은다.

$$Attention(Q,K,V)=\operatorname{softmax}(QK^T/\sqrt{d_k})V$$

## 구현 예제
```python
import torch
q = torch.tensor([[1., 0.], [0., 1.]])
k = q.clone()
v = torch.tensor([[2., 0.], [0., 4.]])
w = torch.softmax(q @ k.T / (k.shape[-1] ** .5), dim=-1)
print(w)
print(w @ v)
```

## 분석
각 행의 가중치 합은 1이다. Attention 가중치는 정보 혼합 비율을 보여주지만 모델 예측의 인과적 설명으로 곧바로 해석할 수는 없다.

## 다음 실험
입력 토큰과 마스킹을 바꾸어 가중치 행렬이 어떻게 변화하는지 시각화한다.
