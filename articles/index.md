---
layout: default
title: "All Articles"
---

<div class="page-banner">
  <h1>All Published Articles</h1>
</div>

<div class="card-grid">
{% for article in site.articles %}
  <a class="card" href="{{ article.url | relative_url }}">
    <h3>{{ article.title }}</h3>
    <p><strong>Authors:</strong>
      {% for author in article.authors %}
        {{ author.name }}{% if forloop.last == false %}, {% endif %}
      {% endfor %}
    </p>
    <p><strong>Issue:</strong> {{ article.issue }}</p>
  </a>
{% endfor %}
</div>
