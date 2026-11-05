---
layout: page
permalink: /publications/
title: Publications
description: Publications and preprints by year. Accepted and forthcoming papers are labeled separately.
nav: false
nav_order: 2
---

[Research by topic]({{ '/' | relative_url }}#research) · [Google Scholar](https://scholar.google.com/citations?user=5d1AHgIAAAAJ)

{% assign sorted_papers = site.data.research_papers | sort: 'sort_date' | reverse %}
{% assign years = sorted_papers | group_by: 'year' %}
{% for year in years %}
### {{ year.name }}

<ul>
{% for paper in year.items %}
{% include research-paper.liquid paper=paper %}
{% endfor %}
</ul>
{% endfor %}
