
---
title: "PyTorch Autograd — 자동 미분의 원리"
date: 2026-11-27
permalink: /posts/pytorch-autograd/
tags:
  - Deep Learning
  - PyTorch
  - Autograd
---

# 1. Introduction

신경망은 어떻게 자신의 가중치를 수정할 수 있을까?

PyTorch의 Autograd는 연산 과정을 기록하고
자동으로 그래디언트를 계산하는 기능이다.

# 2. Core Concepts

- requires_grad
- backward()
- grad
- grad_fn
- detach()
- torch.no_grad()
- Gradient Accumulation

# 3. Implementation

```python
import torch

x = torch.tensor(3.0, requires_grad=True)

y = x ** 2
y.backward()

print(x.grad)
```

실행 결과:

```
tensor(6.)
```

# 4. Analysis

Autograd는 순전파 과정에서 계산 그래프를 구성하고,
역전파를 통해 각 변수의 그래디언트를 계산한다.

# 5. Conclusion

자동 미분은 신경망의 가중치 최적화를 가능하게 하는
딥러닝 프레임워크의 핵심 기능이다.
