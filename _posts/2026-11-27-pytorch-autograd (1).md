---
title: PyTorch Autograd — 신경망은 어떻게 가중치를 수정할까?
date: 2026-11-27 00:00:00 +0900
permalink: /posts/pytorch-autograd/
categories:
- Deep Learning
tags:
- Deep Learning
excerpt: 자동 미분과 그래디언트 누적을 작은 텐서 예제로 이해한다.
---

## 문제 정의
손실 함수가 가중치에 대해 얼마나 민감한지 계산해야 경사하강법을 적용할 수 있다.

## 핵심 원리
`requires_grad=True`는 미분 추적을 요청한다. 연산 결과의 `grad_fn`은 역전파 연산 정보를 나타낸다. `backward()`는 그래디언트를 계산하며 leaf tensor의 `.grad`에 누적한다.

## 구현 및 예상 결과
```python
import torch
x = torch.tensor(3., requires_grad=True)
(x ** 2).backward()
print(x.grad)  # 6
(x ** 2).backward()
print(x.grad)  # 12
x.grad.zero_()
(x ** 2).backward()
print(x.grad)  # 6
```

## 분석
두 번째 backward에서 12가 나오는 이유는 이전 그래디언트에 새 값이 더해지기 때문이다. 일반적인 학습 루프에서는 `optimizer.zero_grad()`를 호출한다. `detach()`는 기존 텐서와 저장공간을 공유할 수 있지만 미분 연결을 끊고, `torch.no_grad()`는 블록 내 역전파 그래프 기록을 비활성화한다.

## 다음 실험
작은 선형 모델에서 손실이 감소하는지 확인하고, 그래디언트를 초기화하지 않았을 때와 비교한다.
