---
title: Soft Actor-Critic (SAC)
excerpt: 최대 엔트로피 강화학습 기반 두 관절 제어 프로젝트
collection: portfolio
permalink: /portfolio/sac/
---

## 1. Project Overview

연속 행동 공간에서 Soft Actor-Critic의 학습 원리를 이해하고 두 관절 시스템을 제어하는 프로젝트이다.

## 2. Problem Definition

아래로 처진 두 관절을 위로 들어 올리고 균형을 유지하는 제어 문제를 목표로 한다.

## 3. Methodology

| 구성 요소 | 역할 |
| --- | --- |
| Actor | 확률적 행동 정책 학습 |
| Twin Critics | 행동 가치 추정 및 과대평가 완화 |
| Replay Buffer | 경험 저장 및 재사용 |
| Target Network | TD 목표 안정화 |
| Entropy | 보상과 탐험의 균형 |
| Reparameterization | 샘플링된 행동을 통한 정책 최적화 |

## 4. Implementation Plan

- 상태, 행동, 보상 및 종료 조건 정의
- Actor와 두 Critic의 학습 과정 구성
- 학습 진행에 따른 보상, Critic Loss, 정책 및 엔트로피 변화 시각화
- 균형 유지 성능 및 실패 사례 평가

## 5. Current Status

이론 및 발표 자료를 정리하고 제어 환경과 실험을 설계하는 단계이다. 실제 균형 유지 시간이나 최종 보상은 검증 후 공개할 예정이다.

## 6. References

- [Soft Actor-Critic, Haarnoja et al. (2018)](https://proceedings.mlr.press/v80/haarnoja18b.html)
