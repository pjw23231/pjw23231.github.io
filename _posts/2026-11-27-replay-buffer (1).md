---
title: 왜 강화학습은 과거 경험을 다시 사용할까?
date: 2026-11-27 00:00:00 +0900
permalink: /posts/replay-buffer/
categories:
- Reinforcement Learning
tags:
- Reinforcement Learning
excerpt: Replay Buffer와 off-policy 학습의 관계를 살펴본다.
---

## 문제 정의
환경과 상호작용한 경험을 한 번만 사용하면 데이터 활용 효율이 낮다. 연속된 경험은 서로 강하게 연관될 수도 있다.

## 핵심 원리
Replay Buffer에는 상태, 행동, 보상, 다음 상태, 종료 여부를 저장한다. 무작위 미니배치는 시간적 상관을 줄이는 데 도움을 준다. SAC는 off-policy 알고리즘이므로 이전 행동 정책으로 수집한 전이를 활용할 수 있다.

## 구현 예제
```python
from collections import deque
import random
buffer = deque(maxlen=1000)
for i in range(10):
    buffer.append((i, 0, 1.0, i+1, False))
batch = random.sample(list(buffer), 4)
print(batch)
```

## 분석
현재 정책이 과거 행동을 다시 선택해야 하는 것은 아니다. Critic은 저장된 행동의 가치와 현재 정책에 따른 다음 행동의 가치를 연결해 학습한다. 다만 데이터 분포가 현재 정책과 지나치게 다르면 학습 품질이 떨어질 수 있다.

## 다음 실험
순차 배치와 무작위 배치의 학습 손실 및 평가 보상을 비교한다.
