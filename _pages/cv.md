---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<style>
  .cv-container {
    --cv-accent: #3b82f6;
    --cv-border: rgba(128, 128, 128, 0.25);
    line-height: 1.7;
  }

  /* Profile Header */

  .cv-header {
    padding: 12px 0 28px;
    margin-bottom: 30px;
    border-bottom: 1px solid var(--cv-border);
  }

  .cv-eyebrow {
    color: var(--cv-accent);
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 1.5px;
    margin-bottom: 12px;
  }

  .cv-name {
    font-size: clamp(1.5rem, 3vw, 2.3rem);
    font-weight: 800;
    line-height: 1.3;
    margin: 0 0 10px;
  }

  .cv-position {
    font-size: 0.95rem;
    opacity: 0.8;
    margin-bottom: 8px;
  }

  .cv-summary {
    font-size: 0.8rem;
    line-height: 1.8;
    opacity: 0.75;
    margin-bottom: 20px;
  }

  .cv-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }

  .cv-container .cv-button {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 18px;
    border: 1px solid var(--cv-border);
    border-radius: 8px;
    color: inherit;
    font-size: 0.78rem;
    font-weight: 600;
    text-decoration: none;
  }

  .cv-container .cv-button-primary {
    background: #2563eb;
    color: white;
    border-color: #2563eb;
  }

  .cv-button:hover {
    opacity: 0.85;
  }

  /* Section Layout */

  .cv-section {
    margin-bottom: 36px;
  }

  .cv-section-title {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 1.3rem;
    font-weight: 750;
    padding-bottom: 12px;
    margin: 0 0 18px;
    border-bottom: 1px solid var(--cv-border);
  }

  .cv-section-title i {
    color: var(--cv-accent);
    font-size: 1.1rem;
  }

  .cv-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 14px;
  }

  .cv-card {
    min-width: 0;
    padding: 20px;
    border: 1px solid var(--cv-border);
    border-radius: 12px;
  }

  .cv-card-title {
    font-size: 0.95rem;
    font-weight: 700;
    margin-bottom: 8px;
  }

  .cv-card-description {
    font-size: 0.8rem;
    line-height: 1.8;
    opacity: 0.8;
    word-break: keep-all;
    overflow-wrap: anywhere;
  }

  /* Education */

  .education-card {
    border-left: 4px solid var(--cv-accent);
  }

  .education-top {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 8px;
  }

  .education-school {
    font-size: 1.1rem;
    font-weight: 750;
  }

  .education-status {
    font-size: 0.65rem;
    padding: 4px 10px;
    border-radius: 5px;
    background: rgba(59, 130, 246, 0.1);
    color: var(--cv-accent);
  }

  .education-degree {
    font-size: 0.9rem;
    margin-bottom: 5px;
  }

  .education-location {
    font-size: 0.75rem;
    opacity: 0.7;
  }

  /* Technical Skills */

  .skill-icon {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 40px;
    height: 40px;
    margin-bottom: 14px;
    border-radius: 10px;
    background: rgba(59, 130, 246, 0.1);
    color: var(--cv-accent);
  }

  .cv-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 7px;
    margin-top: 12px;
  }

  .cv-tag {
    padding: 5px 10px;
    border-radius: 6px;
    border: 1px solid rgba(59, 130, 246, 0.18);
    background: rgba(59, 130, 246, 0.08);
    font-size: 0.7rem;
    font-weight: 500;
  }

  /* Key Achievements */

  .achievement-card {
    text-align: center;
    padding: 24px 16px;
  }

  .achievement-name {
    font-size: 0.8rem;
    font-weight: 600;
    margin-bottom: 12px;
  }

  .achievement-value {
    color: var(--cv-accent);
    font-size: 1.9rem;
    font-weight: 800;
    line-height: 1.2;
    margin-bottom: 8px;
    overflow-wrap: anywhere;
  }

  .achievement-label {
    font-size: 0.72rem;
    opacity: 0.7;
    margin-bottom: 14px;
  }

  .cv-container .cv-link {
    color: var(--cv-accent);
    font-size: 0.78rem;
    font-weight: 600;
    text-decoration: none;
  }

  .cv-link:hover {
    text-decoration: underline;
  }

  /* Portfolio List */

  .cv-project {
    display: flex;
    align-items: flex-start;
    gap: 16px;
    padding: 18px 0;
    border-bottom: 1px solid var(--cv-border);
  }

  .cv-project-number {
    min-width: 28px;
    color: var(--cv-accent);
    font-size: 1rem;
    font-weight: 750;
  }

  .cv-project-body {
    flex: 1;
    min-width: 0;
  }

  .cv-project-title {
    font-size: 0.9rem;
    font-weight: 700;
    margin-bottom: 5px;
  }

  .cv-project-title a {
    color: inherit;
    text-decoration: none;
  }

  .cv-project-title a:hover {
    color: var(--cv-accent);
  }

  .cv-project-description {
    font-size: 0.75rem;
    line-height: 1.7;
    opacity: 0.75;
  }

  .cv-project-arrow {
    color: var(--cv-accent);
    text-decoration: none;
    font-size: 0.85rem;
  }

  .cv-view-all {
    margin-top: 18px;
    text-align: right;
  }

  /* Activities */

  .cv-activity {
    display: flex;
    align-items: flex-start;
    gap: 14px;
    margin-bottom: 14px;
    padding: 16px;
    border: 1px solid var(--cv-border);
    border-radius: 10px;
  }

  .cv-activity-icon {
    color: var(--cv-accent);
    font-size: 1rem;
    min-width: 22px;
  }

  .cv-activity-title {
    font-size: 0.85rem;
    font-weight: 700;
    margin-bottom: 4px;
  }

  .cv-activity-description {
    font-size: 0.75rem;
    opacity: 0.75;
  }

  /* Career Goal */

  .cv-career {
    padding: 22px;
    border: 1px solid var(--cv-border);
    border-left: 4px solid var(--cv-accent);
    border-radius: 10px;
  }

  /* Responsive Design */

  @media (max-width: 768px) {
    .cv-grid {
      grid-template-columns: 1fr;
    }

    .cv-card {
      padding: 16px;
    }

    .cv-name {
      font-size: 1.6rem;
    }

    .cv-project {
      gap: 10px;
    }
  }

  /* Print Layout */

  @media print {
    .cv-actions,
    .cv-view-all,
    .cv-project-arrow {
      display: none !important;
    }

    .cv-card,
    .cv-project,
    .cv-activity,
    .cv-career {
      break-inside: avoid;
    }
  }
</style>

<div class="cv-container">

  <!-- 1. Profile Header -->

  <header class="cv-header">

    <div class="cv-eyebrow">
      CURRICULUM VITAE
    </div>

    <h1 class="cv-name">
      PARK JIWAN (박지완)
    </h1>

    <div class="cv-position">
      AI Undergraduate Student
    </div>

    <div class="cv-summary">
      Machine Learning &middot;
      Deep Learning &middot;
      Data Science &middot;
      Financial AI
    </div>

    <div class="cv-actions">

      <a class="cv-button cv-button-primary"
         href="https://github.com/pjw23231">
        <i class="fab fa-github" aria-hidden="true"></i>
        GitHub Profile
      </a>

      <a class="cv-button"
         href="mailto:pjw23231@gmail.com">
        <i class="fas fa-envelope" aria-hidden="true"></i>
        Contact Me
      </a>

      <button type="button"
              class="cv-button"
              onclick="window.print()">
        <i class="fas fa-print" aria-hidden="true"></i>
        Print CV
      </button>

    </div>

  </header>


  <!-- 2. Education -->

  <section class="cv-section">

    <h2 class="cv-section-title">
      <i class="fas fa-graduation-cap"
         aria-hidden="true"></i>
      Education
    </h2>

    <div class="cv-card education-card">

      <div class="education-top">

        <div class="education-school">
          Jeonju University
        </div>

        <span class="education-status">
          In Progress
        </span>

      </div>

      <div class="education-degree">
        B.S. in Artificial Intelligence
      </div>

      <div class="education-location">
        Jeonju, South Korea
      </div>

    </div>

  </section>


  <!-- 3. Research Interests -->

  <section class="cv-section">

    <h2 class="cv-section-title">
      <i class="fas fa-search" aria-hidden="true"></i>
      Research Interests
    </h2>

    <div class="cv-tags">
      <span class="cv-tag">Machine Learning</span>
      <span class="cv-tag">Deep Learning</span>
      <span class="cv-tag">Reinforcement Learning</span>
      <span class="cv-tag">Natural Language Processing</span>
      <span class="cv-tag">Financial Data Analysis</span>
      <span class="cv-tag">Data Visualization</span>
      <span class="cv-tag">Predictive Analytics</span>
    </div>

  </section>


  <!-- 4. Technical Skills -->

  <section class="cv-section">

    <h2 class="cv-section-title">
      <i class="fas fa-code" aria-hidden="true"></i>
      Technical Skills
    </h2>

    <div class="cv-grid">

      <div class="cv-card">

        <div class="skill-icon">
          <i class="fas fa-terminal"
             aria-hidden="true"></i>
        </div>

        <div class="cv-card-title">
          Programming
        </div>

        <div class="cv-card-description">
          데이터 처리 및 AI 모델 구현을 위한 프로그래밍
        </div>

        <div class="cv-tags">
          <span class="cv-tag">Python</span>
        </div>

      </div>


      <div class="cv-card">

        <div class="skill-icon">
          <i class="fas fa-brain"
             aria-hidden="true"></i>
        </div>

        <div class="cv-card-title">
          AI &amp; Machine Learning
        </div>

        <div class="cv-card-description">
          인공지능 모델 구현, 학습 및 성능 평가
        </div>

        <div class="cv-tags">
          <span class="cv-tag">PyTorch</span>
          <span class="cv-tag">TensorFlow</span>
          <span class="cv-tag">Keras</span>
          <span class="cv-tag">Scikit-learn</span>
        </div>

      </div>


      <div class="cv-card">

        <div class="skill-icon">
          <i class="fas fa-chart-bar"
             aria-hidden="true"></i>
        </div>

        <div class="cv-card-title">
          Data Analysis &amp; Visualization
        </div>

        <div class="cv-card-description">
          데이터 전처리, 탐색적 분석 및 결과 시각화
        </div>

        <div class="cv-tags">
          <span class="cv-tag">NumPy</span>
          <span class="cv-tag">Pandas</span>
          <span class="cv-tag">Matplotlib</span>
          <span class="cv-tag">Seaborn</span>
        </div>

      </div>


      <div class="cv-card">

        <div class="skill-icon">
          <i class="fas fa-tools"
             aria-hidden="true"></i>
        </div>

        <div class="cv-card-title">
          Development Environment
        </div>

        <div class="cv-card-description">
          개발 환경 구성, 버전 관리 및 프로젝트 실습
        </div>

        <div class="cv-tags">
          <span class="cv-tag">Git</span>
          <span class="cv-tag">GitHub</span>
          <span class="cv-tag">VS Code</span>
          <span class="cv-tag">Ubuntu</span>
          <span class="cv-tag">WSL2</span>
          <span class="cv-tag">Docker</span>
          <span class="cv-tag">ROS2</span>
        </div>

      </div>

    </div>

  </section>


  <!-- 5. Key Achievements -->

  <section class="cv-section">

    <h2 class="cv-section-title">
      <i class="fas fa-trophy" aria-hidden="true"></i>
      Key Achievements
    </h2>

    <div class="cv-grid">

      <div class="cv-card achievement-card">

        <div class="achievement-name">
          MNIST Classification
        </div>

        <div class="achievement-value">
          99.675%
        </div>

        <div class="achievement-label">
          Kaggle Accuracy
        </div>

        <a class="cv-link"
           href="{{ '/portfolio/mnist/' | relative_url }}">
          View Project &rarr;
        </a>

      </div>


      <div class="cv-card achievement-card">

        <div class="achievement-name">
          Iceberg Classification
        </div>

        <div class="achievement-value">
          0.07436
        </div>

        <div class="achievement-label">
          Private Leaderboard Log Loss
        </div>

        <a class="cv-link"
           href="{{ '/portfolio/iceberg/' | relative_url }}">
          View Project &rarr;
        </a>

      </div>

    </div>

  </section>


  <!-- 6. Automatically Updated Portfolio -->

  <section class="cv-section">

    <h2 class="cv-section-title">
      <i class="fas fa-folder-open"
         aria-hidden="true"></i>
      Portfolio ({{ site.portfolio | size }})
    </h2>

    {% for post in site.portfolio %}

      <article class="cv-project">

        <div class="cv-project-number">
          {% if forloop.index < 10 %}0{% endif %}{{ forloop.index }}
        </div>

        <div class="cv-project-body">

          <div class="cv-project-title">
            <a href="{{ post.url | relative_url }}">
              {{ post.title | escape }}
            </a>
          </div>

          <div class="cv-project-description">
            {{ post.excerpt
               | strip_html
               | normalize_whitespace
               | truncate: 150
               | escape }}
          </div>

        </div>

        <a class="cv-project-arrow"
           href="{{ post.url | relative_url }}"
           aria-label="View {{ post.title | escape }}">
          &nearr;
        </a>

      </article>

    {% endfor %}

    <div class="cv-view-all">
      <a class="cv-link"
         href="{{ '/portfolio/' | relative_url }}">
        View All Projects &rarr;
      </a>
    </div>

  </section>


  <!-- 7. Presentations -->

  <section class="cv-section">

    <h2 class="cv-section-title">
      <i class="fas fa-chalkboard-teacher"
         aria-hidden="true"></i>
      Presentations
    </h2>

    <div class="cv-card">

      <div class="cv-card-title">
        Soft Actor-Critic (SAC)
      </div>

      <div class="cv-card-description">
        Actor-Critic 구조와 최대 엔트로피 강화학습의
        핵심 원리를 학습하고, 연속 행동 제어에
        적용하는 발표 프로젝트
      </div>

      <div class="cv-tags">
        <span class="cv-tag">Actor-Critic</span>
        <span class="cv-tag">Replay Buffer</span>
        <span class="cv-tag">Target Network</span>
        <span class="cv-tag">Twin Critics</span>
        <span class="cv-tag">Maximum Entropy</span>
      </div>

    </div>

  </section>


  <!-- 8. Activities -->

  <section class="cv-section">

    <h2 class="cv-section-title">
      <i class="fas fa-users" aria-hidden="true"></i>
      Activities
    </h2>

    <div class="cv-activity">

      <div class="cv-activity-icon">
        <i class="fas fa-trophy" aria-hidden="true"></i>
      </div>

      <div>
        <div class="cv-activity-title">
          Kaggle Machine Learning Competitions
        </div>

        <div class="cv-activity-description">
          이미지 분류 모델 학습 및 성능 최적화 실험
        </div>
      </div>

    </div>


    <div class="cv-activity">

      <div class="cv-activity-icon">
        <i class="fas fa-university"
           aria-hidden="true"></i>
      </div>

      <div>
        <div class="cv-activity-title">
          University AI Projects
        </div>

        <div class="cv-activity-description">
          딥러닝, 자연어 처리 및 강화학습 프로젝트
        </div>
      </div>

    </div>


    <div class="cv-activity">

      <div class="cv-activity-icon">
        <i class="fas fa-chart-line"
           aria-hidden="true"></i>
      </div>

      <div>
        <div class="cv-activity-title">
          Data Analysis Projects
        </div>

        <div class="cv-activity-description">
          데이터 전처리, 분석 및 시각화 실습
        </div>
      </div>

    </div>


    <div class="cv-activity">

      <div class="cv-activity-icon">
        <i class="fas fa-blog"
           aria-hidden="true"></i>
      </div>

      <div>
        <div class="cv-activity-title">
          Technical Blogging
        </div>

        <div class="cv-activity-description">
          AI 및 데이터 분석 학습 과정과 문제 해결 기록
        </div>
      </div>

    </div>

  </section>


  <!-- 9. Career Goal -->

  <section class="cv-section">

    <h2 class="cv-section-title">
      <i class="fas fa-bullseye"
         aria-hidden="true"></i>
      Career Goal
    </h2>

    <div class="cv-career">

      <div class="cv-card-title">
        AI &amp; Financial Data Analysis
      </div>

      <div class="cv-card-description">
        인공지능과 금융 데이터를 결합하여
        데이터 기반 의사결정에 기여하는 것을
        목표로 합니다.
        <br><br>
        머신러닝 기반 예측, 금융 정보 분석,
        데이터 시각화 및 모델 결과 해석 역량을
        지속적으로 발전시키고자 합니다.
      </div>

    </div>

  </section>

</div>
