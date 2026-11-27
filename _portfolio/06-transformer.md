---
title: Transformer for Machine Translation
excerpt: Attention 기반 영어-한국어 번역 모델 학습 및 구현 실습
collection: portfolio
permalink: /portfolio/transformer/
---

## 1. Project Overview

Transformer의 Encoder-Decoder 구조를 이해하고 영어-한국어 기계 번역을 위한 데이터 처리 및 모델 구현을 학습하는 프로젝트이다.

## 2. Problem Definition

입력 문장의 문맥과 단어 간 관계를 학습하여 의미를 보존하는 목표 언어 문장을 생성한다.

## 3. Methodology

| 구성 요소 | 역할 |
| --- | --- |
| SentencePiece | 서브워드 토큰화 |
| Embedding / Positional Encoding | 토큰 및 위치 정보 표현 |
| Multi-Head Attention | 다양한 관계 학습 |
| Masked Self-Attention | 미래 정답 정보 차단 |
| Cross-Attention | 입력 문장 정보 활용 |
| Feed-Forward Network | 토큰별 특징 변환 |

## 4. Implementation Workflow

1. 병렬 문장 데이터 전처리
2. 토크나이저 구성
3. 학습·검증 데이터 분리
4. Encoder-Decoder 및 마스크 구현
5. 학습과 자동회귀 번역 생성 실험

## 5. Current Status

Transformer의 구성 요소를 학습하고 데이터 전처리 및 토큰화 실습을 진행하였다. 최종 번역 결과와 BLEU 등 평가 지표는 실험 완료 후 추가할 예정이다.

## 6. Future Improvements

- 번역 오류와 문맥 보존 여부 분석
- Attention 시각화
- 학습 곡선 및 번역 품질 비교

## 7. References

- [Attention Is All You Need](https://arxiv.org/abs/1706.03762)
