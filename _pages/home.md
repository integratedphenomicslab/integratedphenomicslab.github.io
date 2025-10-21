---
layout: about
title: Welcome
permalink: /
nav: False

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: true
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

<div class="header-bar">
  <h1>{{ site.title }}</h1>
  <h2>{{ site.description }}</h2>
  {% include blog_tags.html %}
</div>


## Key Research Areas
- Computational Phenotyping
- AI in Medical Genomics
- Multimodal Data Integration

[meet the team](/about/).
