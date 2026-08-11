---
permalink: /
title: "Homepage"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi there!  I am Jiale Chen, currently pursuing my Ph.D. in Software Engineering at Hohai University since 2023, supervised by Prof. Feng Xu and co-supervised by Associate Prof. Xin Lv and Associate Prof. Xin Li.

My research focuses on few-shot learning, particularly in finegrained image classification, multi-modal learning, cross-domain adaptation, and class-incremental learning. I aim to develop a sustainable few-shot learning framework that integrates advanced AI techniques with real-world applications. This framework is designed to quickly adapt to niche domains or flexible tasks, especially those with limited data and challenging sampling conditions.

I'm always eager to learn and improve, so I warmly welcome any suggestions or guidance from fellow researchers. Feel free to reach out via email! 😊

## Publications

{% assign sorted_pubs = site.publications | sort: 'date' | reverse %}
{% for post in sorted_pubs %}
  {% if post.citation contains 'Jiale Chen,' %}
    {% assign authors_short = '<strong>Jiale Chen</strong> et al.' %}
  {% else %}
    {% assign authors_short = '<strong>Jiale Chen</strong>' %}
  {% endif %}
- {{ authors_short }}. <a href="{{ post.url | relative_url }}"><em>{{ post.title }}</em></a>, <strong>{{ post.venue }}</strong>, {{ post.date | date: "%Y" }}.
{% endfor %}
