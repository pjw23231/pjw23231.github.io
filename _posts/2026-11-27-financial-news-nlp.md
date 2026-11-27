---
title: 금융 뉴스의 복잡한 정보를 한눈에 보여줄 수 있을까?
date: 2026-11-27 00:00:00 +0900
permalink: /posts/financial-news-nlp/
categories:
- Financial Data Analysis
tags:
- Financial Data Analysis
excerpt: 금융 뉴스 정보 추출 및 시각화 프로젝트 설계 초안.
---

## 문제 정의
긴 금융 기사에서 핵심 사건과 수치, 관련 자산을 빠르게 찾기 어렵다.

## 설계 방향
기사 수집 및 정제 → 개체·수치 추출 → 요약 → 출처 연결 → 시각화 순서로 구성한다. 사실과 해석을 분리하고, 원문과 날짜를 유지한다.

## 구현 예제: 입력 형식
```python
article = {'title': '예시 기사', 'source': 'example', 'date': '2026-11-27', 'text': '매출이 5% 증가했다.'}
import re
print(re.findall(r'\d+(?:\.\d+)?%', article['text']))
```

## 분석
정규식은 수치를 찾을 수 있지만 수치의 대상, 부호, 맥락을 이해하지 못한다. 요약 모델 역시 사실 오류를 만들 수 있다. 원문 대조와 평가 데이터가 필요하다.

## 다음 실험
기사별 핵심 사실 추출 정확도와 요약 충실도를 평가하는 데이터셋을 설계한다. 현재는 기획 단계이다.
