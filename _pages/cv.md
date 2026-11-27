---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======

* Jeonju University, Jeonju, South Korea
  * B.S. in Artificial Intelligence (in progress)

Research Interests
======

* Deep Learning
* Reinforcement Learning
* Natural Language Processing
* Financial Data Analysis
* Machine Learning Applications

Technical Skills
======

* Programming
  * Python

* Artificial Intelligence
  * PyTorch
  * TensorFlow / Keras
  * Scikit-learn

* Data Analysis & Visualization
  * NumPy
  * Pandas
  * Matplotlib

* Development Environment
  * Git / GitHub
  * Ubuntu / WSL2
  * Docker
  * ROS2

Portfolio
======

<ul>
{% for post in site.portfolio reversed %}
  <li>
    <a href="{{ post.url | relative_url }}">
      {{ post.title }}
    </a>
    <p>{{ post.excerpt | strip_html }}</p>
  </li>
{% endfor %}
</ul>

Presentations
======

* Soft Actor-Critic (SAC)
  * Actor-Critic Architecture
  * Maximum Entropy Reinforcement Learning
  * Continuous Control

Activities
======

* Kaggle Machine Learning Competitions
* University AI Projects
* Data Analysis Projects
* Technical Blogging
