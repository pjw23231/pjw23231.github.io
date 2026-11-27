---
title: GitHub Pages — Commit했는데 왜 홈페이지가 바뀌지 않을까?
date: 2026-11-27 00:00:00 +0900
permalink: /posts/github-pages/
categories:
- Development
tags:
- Development
excerpt: 실제 블로그 구축 과정에서 만난 Git 및 Jekyll 문제를 정리한다.
---

## 문제 정의
VS Code에서 Commit을 했지만 홈페이지가 갱신되지 않았다. 이후 CV 경로에서 404도 발생했다.

## 원인 및 해결
Commit은 로컬 변경 이력을 기록한다. Push는 원격 저장소에 전송한다. `ahead of origin/master by 1 commit`은 전송되지 않은 커밋이 있다는 의미다.

```bash
git status
git push origin master
```

Jekyll 페이지의 Front Matter는 파일 맨 첫 줄의 `---`부터 시작해야 한다. CV의 선행 빈 줄을 제거한 뒤 정상적으로 표시되었다. 설정 파일 교체 시 `_pages`를 포함하는 `include` 등 기존 설정도 보존해야 한다.

## 확인 방법
GitHub Actions의 최신 커밋과 배포 성공 여부를 확인한 뒤 실제 페이지를 새로고침한다. 빌드 성공이 모든 페이지의 정상 생성을 보장하는 것은 아니다.

## 배운 점
파일 저장, Commit, Push, Build, Deploy를 서로 다른 단계로 구분하면 문제 원인을 빠르게 좁힐 수 있다.
