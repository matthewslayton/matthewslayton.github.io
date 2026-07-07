---
layout: page
permalink: /repositories/
title: Repositories
description: Check back soon! I'll make my more repos public after I finish checking for PHI
nav: true
nav_order: 2
---

## GitHub Activity

{% if site.data.github_stats %}
{{ site.data.github_stats.commits_last_year }} commits ({{ site.data.github_stats.contributions_last_year }} total contributions) in the last year as of {{ site.data.github_stats.generated_at | date: "%B %-d, %Y" }}
{% endif %}

---

## GitHub Repositories

{% if site.data.repositories.github_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}
