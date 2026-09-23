---
layout: default
---

## Projects

{% assign repos = site.github.public_repositories | where: "has_pages", true | sort: "name" %}
{% for repo in repos %}{% unless repo.name == site.github.repository_name %}
### [{{ repo.name }}]({{ site.github.url }}/{{ repo.name }}/)

{% if repo.description %}{{ repo.description }}{% endif %}

[Source]({{ repo.html_url }}){% if repo.language %} · {{ repo.language }}{% endif %}
{% endunless %}{% endfor %}
