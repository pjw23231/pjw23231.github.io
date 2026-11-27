
---
layout: single
permalink: /
title: ""
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<style>
  /* About Page Layout */

  .about-home {
    --accent: #3b82f6;
    --border: rgba(128, 128, 128, 0.25);
    line-height: 1.7;
  }

  /* Hero Section */

  .about-hero {
    padding: 24px 0 32px;
    margin-bottom: 24px;
  }

  .about-eyebrow {
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 1.6px;
    color: var(--accent);
    margin-bottom: 18px;
  }

  .about-headline {
    font-size: clamp(1.8rem, 3.5vw, 2.8rem);
    font-weight: 800;
    line-height: 1.2;
    letter-spacing: -1px;
    margin: 0 0 22px;
  }

  .about-highlight {
    color: var(--accent);
  }

  .about-description {
    font-size: 0.95rem;
    line-height: 1.9;
    opacity: 0.85;
    margin-bottom: 24px;
    word-break: keep-all;
    overflow-wrap: anywhere;
  }

  /* Navigation Buttons */

  .about-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }

  .about-home .about-btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 11px 20px;
    border-radius: 8px;
    font-size: 0.8rem;
    font-weight: 600;
    text-decoration: none;
    transition: transform 0.2s ease;
  }

  .about-home .about-btn-primary {
    background: #2563eb;
    color: #ffffff;
    border: 1px solid #2563eb;
  }

  .about-home .about-btn-secondary {
    border: 1px solid var(--border);
    color: inherit;
  }

  .about-btn:hover {
    transform: translateY(-2px);
  }

  /* Statistics */

  .about-stats {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 12px;
    margin-bottom: 42px;
  }

  .about-stat {
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px 10px;
    text-align: center;
  }

  .about-stat-value {
    display: block;
    color: var(--accent);
    font-size: 1.8rem;
    font-weight: 750;
  }

  .about-stat-label {
    display: block;
    font-size: 0.72rem;
    opacity: 0.75;
    margin-top: 5px;
  }

  /* Section Layout */

  .about-section {
    margin-bottom: 42px;
  }

  .about-section-title {
    font-size: 1.4rem;
    font-weight: 750;
    margin: 0 0 20px;
    padding-bottom: 12px;
    border-bottom: 1px solid var(--border);
  }

  .about-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 14px;
  }

  /* Interest Cards */

  .interest-card {
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    min-width: 0;
    transition: border-color 0.2s ease,
                transform 0.2s ease;
  }

  .interest-card:hover {
    transform: translateY(-3px);
    border-color: var(--accent);
  }

  .interest-icon {
    display: flex;
    align-items: center;
    justify-content: center;
    background: rgba(59, 130, 246, 0.1);
    color: var(--accent);
    width: 40px;
    height: 40px;
    border-radius: 10px;
    font-size: 1rem;
    margin-bottom: 14px;
  }

  .interest-name {
    font-size: 0.9rem;
    font-weight: 700;
    margin-bottom: 6px;
  }

  .interest-description {
    font-size: 0.78rem;
    line-height: 1.7;
    opacity: 0.75;
    word-break: keep-all;
    overflow-wrap: anywhere;
  }

  /* Featured Projects */

  .featured-card {
    display: flex;
    flex-direction: column;
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 22px;
    min-width: 0;
    transition: transform 0.2s ease,
                border-color 0.2s ease;
  }

  .featured-card:hover {
    transform: translateY(-3px);
    border-color: var(--accent);
  }

  .featured-category {
    color: var(--accent);
    font-size: 0.65rem;
    font-weight: 700;
    letter-spacing: 1px;
    margin-bottom: 12px;
  }

  .featured-title {
    font-size: 0.95rem;
    font-weight: 700;
    margin-bottom: 16px;
  }

  .featured-metric {
    color: var(--accent);
    font-size: 1.8rem;
    font-weight: 800;
    line-height: 1.2;
  }

  .featured-label {
    font-size: 0.72rem;
    opacity: 0.7;
    margin-top: 5px;
    margin-bottom: 16px;
  }

  .featured-description {
    font-size: 0.8rem;
    line-height: 1.7;
    opacity: 0.8;
    margin-bottom: 18px;
  }

  .featured-footer {
    margin-top: auto;
    padding-top: 12px;
    border-top: 1px solid var(--border);
  }

  .about-home .about-link {
    font-size: 0.8rem;
    font-weight: 600;
    color: var(--accent);
    text-decoration: none;
  }

  .about-link:hover {
    text-decoration: underline;
  }

  /* Latest Articles */

  .latest-article {
    padding: 16px 0;
    border-bottom: 1px solid var(--border);
  }

  .article-category {
    font-size: 0.65rem;
    color: var(--accent);
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.6px;
    margin-bottom: 6px;
  }

  .article-title {
    font-size: 0.95rem;
    font-weight: 700;
    margin-bottom: 6px;
  }

  .article-title a {
    color: inherit;
    text-decoration: none;
  }

  .article-title a:hover {
    color: var(--accent);
  }

  .article-description {
    font-size: 0.78rem;
    opacity: 0.75;
    margin-bottom: 7px;
  }

  .article-date {
    font-size: 0.7rem;
    opacity: 0.6;
  }

  .about-view-all {
    margin-top: 18px;
    text-align: right;
  }

  /* Career Goal */

  .career-box {
    border: 1px solid var(--border);
    border-left: 4px solid var(--accent);
    border-radius: 10px;
    padding: 24px;
  }

  .career-heading {
    font-size: 1.05rem;
    font-weight: 700;
    margin-bottom: 12px;
  }

  .career-description {
    font-size: 0.85rem;
    line-height: 1.9;
    opacity: 0.85;
    word-break: keep-all;
  }

  /* Technology Tags */

  .about-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 18px;
  }

  .about-tag {
    padding: 5px 11px;
    font-size: 0.7rem;
    border-radius: 6px;
    background: rgba(59, 130, 246, 0.09);
    border: 1px solid rgba(59, 130, 246, 0.18);
  }

  /* Learning Process */

  .learning-flow {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 10px;
  }

  .learning-step {
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 16px 12px;
  }

  .step-number {
    font-size: 1.2rem;
    color: var(--accent);
    font-weight: 800;
    margin-bottom: 5px;
  }

  .step-title {
    font-size: 0.85rem;
    font-weight: 700;
    margin-bottom: 5px;
  }

  .step-description {
    font-size: 0.72rem;
    opacity: 0.75;
  }

  /* Responsive Design */

  @media (max-width: 768px) {
    .about-grid {
      grid-template-columns: 1fr;
    }

    .about-stats {
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 7px;
    }

    .about-stat-value {
      font-size: 1.4rem;
    }

    .about-stat-label {
      font-size: 0.65rem;
    }

    .learning-flow {
      grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .about-hero {
      padding-top: 10px;
    }
  }

  @media (prefers-reduced-motion: reduce) {
    .about-btn,
    .interest-card,
    .featured-card {
      transition: none;
    }

    .about-btn:hover,
    .interest-card:hover,
    .featured-card:hover {
      transform: none;
    }
  }
</style>

<div class="about-home">

  <!-- 1. Hero Section -->

  <section class="about-hero">

    <div class="about-eyebrow">
      ARTIFICIAL INTELLIGENCE &middot; DATA SCIENCE
    </div>

    <h1 class="about-headline">
      Turning Data into Insights.<br>
      <span class="about-highlight">
        Insights into Decisions.
      </span>
    </h1>

    <div class="about-description">
      안녕하세요. 전주대학교 인공지능학과에 재학 중인
      박지완(PARK JIWAN)입니다.
      <br><br>
      인공지능과 데이터 분석을 통해 복잡한 문제를 이해하고,
      데이터에서 의미 있는 정보를 발견하며,
      이를 실제 의사결정에 활용하는 방법을 탐구합니다.
      특히 머신러닝과 금융 데이터 분석에 관심을 가지고 있습니다.
    </div>

    <div class="about-actions">

      <a class="about-btn about-btn-primary"
         href="{{ '/portfolio/' | relative_url }}">
        View Projects &rarr;
      </a>

      <a class="about-btn about-btn-secondary"
         href="{{ '/cv/' | relative_url }}">
        View CV
      </a>

      <a class="about-btn about-btn-secondary"
         href="{{ '/year-archive/' | relative_url }}">
        Read Blog
      </a>

    </div>

  </section>


  <!-- 2. Automatic Statistics -->

  <div class="about-stats">

    <div class="about-stat">
      <span class="about-stat-value">
        {{ site.portfolio | size }}
      </span>
      <span class="about-stat-label">
        Projects
      </span>
    </div>

    <div class="about-stat">
      <span class="about-stat-value">
        {{ site.posts | size }}
      </span>
      <span class="about-stat-label">
        Articles
      </span>
    </div>

    <div class="about-stat">
      <span class="about-stat-value">
        {{ site.categories | size }}
      </span>
      <span class="about-stat-label">
        Categories
      </span>
    </div>

  </div>


  <!-- 3. Areas of Interest -->

  <section class="about-section">

    <h2 class="about-section-title">
      Areas of Interest
    </h2>

    <div class="about-grid">

      <div class="interest-card">
        <div class="interest-icon">
          <i class="fas fa-brain" aria-hidden="true"></i>
        </div>
        <div class="interest-name">
          Machine Learning
        </div>
        <div class="interest-description">
          데이터 기반 학습과 예측 모델을 연구하고
          모델의 일반화 성능을 탐구합니다.
        </div>
      </div>

      <div class="interest-card">
        <div class="interest-icon">
          <i class="fas fa-network-wired"
             aria-hidden="true"></i>
        </div>
        <div class="interest-name">
          Deep Learning
        </div>
        <div class="interest-description">
          신경망 구조와 학습 원리를 이해하고
          모델의 성능을 개선하는 방법을 탐구합니다.
        </div>
      </div>

      <div class="interest-card">
        <div class="interest-icon">
          <i class="fas fa-robot" aria-hidden="true"></i>
        </div>
        <div class="interest-name">
          Reinforcement Learning
        </div>
        <div class="interest-description">
          보상 기반 의사결정과 연속 행동 제어,
          Actor-Critic 알고리즘을 학습합니다.
        </div>
      </div>

      <div class="interest-card">
        <div class="interest-icon">
          <i class="fas fa-language" aria-hidden="true"></i>
        </div>
        <div class="interest-name">
          Natural Language Processing
        </div>
        <div class="interest-description">
          자연어 이해, Attention, Transformer를 활용한
          텍스트 분석 및 정보 추출에 관심이 있습니다.
        </div>
      </div>

      <div class="interest-card">
        <div class="interest-icon">
          <i class="fas fa-chart-line"
             aria-hidden="true"></i>
        </div>
        <div class="interest-name">
          Financial Data Analysis
        </div>
        <div class="interest-description">
          금융 데이터와 머신러닝을 결합하여
          데이터 기반 의사결정 방법을 탐구합니다.
        </div>
      </div>

      <div class="interest-card">
        <div class="interest-icon">
          <i class="fas fa-chart-bar"
             aria-hidden="true"></i>
        </div>
        <div class="interest-name">
          Data Visualization
        </div>
        <div class="interest-description">
          복잡한 데이터와 분석 결과를
          직관적이고 이해하기 쉬운 형태로 표현합니다.
        </div>
      </div>

    </div>

  </section>


  <!-- 4. Featured Projects -->

  <section class="about-section">

    <h2 class="about-section-title">
      Featured Projects
    </h2>

    <div class="about-grid">

      <article class="featured-card">

        <div class="featured-category">
          COMPUTER VISION
        </div>

        <div class="featured-title">
          MNIST Image Classification
        </div>

        <div class="featured-metric">
          99.675%
        </div>

        <div class="featured-label">
          Kaggle Accuracy
        </div>

        <div class="featured-description">
          CNN 기반 손글씨 숫자 분류 모델의
          구조 및 학습 전략 최적화 프로젝트
        </div>

        <div class="featured-footer">
          <a class="about-link"
             href="{{ '/portfolio/mnist/' | relative_url }}">
            View Project &rarr;
          </a>
        </div>

      </article>


      <article class="featured-card">

        <div class="featured-category">
          COMPUTER VISION
        </div>

        <div class="featured-title">
          Iceberg Classification
        </div>

        <div class="featured-metric">
          0.07436
        </div>

        <div class="featured-label">
          Private Leaderboard Log Loss
        </div>

        <div class="featured-description">
          SAR 이미지를 활용한 빙산 및 선박 분류,
          TTA와 Pseudo-labeling 기반 성능 개선
        </div>

        <div class="featured-footer">
          <a class="about-link"
             href="{{ '/portfolio/iceberg/' | relative_url }}">
            View Project &rarr;
          </a>
        </div>

      </article>

    </div>

    <div class="about-view-all">
      <a class="about-link"
         href="{{ '/portfolio/' | relative_url }}">
        View All Projects &rarr;
      </a>
    </div>

  </section>


  <!-- 5. Automatically Updated Latest Articles -->

  <section class="about-section">

    <h2 class="about-section-title">
      Latest Articles
    </h2>

    {% for post in site.posts limit: 3 %}

      <article class="latest-article">

        <div class="article-category">
          {{ post.categories | join: " / " | escape }}
        </div>

        <div class="article-title">

          <a href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>

        </div>

        <div class="article-description">

          {{ post.excerpt
             | strip_html
             | normalize_whitespace
             | truncate: 120
             | escape }}

        </div>

        <div class="article-date">
          {{ post.date | date: "%Y.%m.%d" }}
        </div>

      </article>

    {% endfor %}

    <div class="about-view-all">
      <a class="about-link"
         href="{{ '/year-archive/' | relative_url }}">
        View All Articles &rarr;
      </a>
    </div>

  </section>


  <!-- 6. Learning Philosophy -->

  <section class="about-section">

    <h2 class="about-section-title">
      How I Learn
    </h2>

    <div class="about-description">
      단순히 알고리즘을 사용하는 것에 그치지 않고,
      왜 필요한지 이해하고 직접 구현하며
      결과를 분석하는 학습 방식을 지향합니다.
    </div>

    <div class="learning-flow">

      <div class="learning-step">
        <div class="step-number">01</div>
        <div class="step-title">Problem</div>
        <div class="step-description">문제 발견 및 정의</div>
      </div>

      <div class="learning-step">
        <div class="step-number">02</div>
        <div class="step-title">Understanding</div>
        <div class="step-description">핵심 원리 이해</div>
      </div>

      <div class="learning-step">
        <div class="step-number">03</div>
        <div class="step-title">Implementation</div>
        <div class="step-description">알고리즘 및 코드 구현</div>
      </div>

      <div class="learning-step">
        <div class="step-number">04</div>
        <div class="step-title">Experiment</div>
        <div class="step-description">실험 및 성능 검증</div>
      </div>

      <div class="learning-step">
        <div class="step-number">05</div>
        <div class="step-title">Analysis</div>
        <div class="step-description">결과 및 원인 분석</div>
      </div>

      <div class="learning-step">
        <div class="step-number">06</div>
        <div class="step-title">Improvement</div>
        <div class="step-description">개선 방향 탐색</div>
      </div>

    </div>

  </section>


  <!-- 7. Career Goal -->

  <section class="about-section">

    <h2 class="about-section-title">
      Career Goal
    </h2>

    <div class="career-box">

      <div class="career-heading">
        Connecting Artificial Intelligence and Finance
      </div>

      <div class="career-description">
        AI 기술과 금융 데이터를 결합하여
        데이터 기반 의사결정에 기여하는 것을 목표로 합니다.
        <br><br>
        단순히 높은 예측 성능을 얻는 것뿐만 아니라,
        모델이 어떤 근거로 결과를 도출하는지 이해하고
        실제 금융 문제에 적용할 수 있는 분석 역량을
        발전시키고자 합니다.
      </div>

      <div class="about-tags">
        <span class="about-tag">Machine Learning</span>
        <span class="about-tag">Financial Data</span>
        <span class="about-tag">Predictive Analytics</span>
        <span class="about-tag">NLP</span>
        <span class="about-tag">Data Visualization</span>
      </div>

    </div>

  </section>

</div>
