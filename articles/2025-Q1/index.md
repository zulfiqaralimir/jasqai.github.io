## Articles Published in This Issue

<div class="card-grid">
{% assign issue_name = "Volume 1, Issue 1 (Q1 2025)" %}

{% for article in site.articles %}
  {% if article.issue == issue_name %}
    <a class="card" href="{{ article.url | relative_url }}">
      <h3>{{ article.title }}</h3>
      <p><strong>Authors:</strong>
        {% for author in article.authors %}
          {{ author.name }}{% if forloop.last == false %}, {% endif %}
        {% endfor %}
      </p>
    </a>
  {% endif %}
{% endfor %}
</div>
