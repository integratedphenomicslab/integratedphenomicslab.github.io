---
layout: about
title: WELCOME
permalink: /
nav: False

selected_papers: false # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

<div class="header-bar">
  <h1>{{ site.title }}</h1>
  <h2>{{ site.description }}</h2>
</div>

{% if site.display_tags and site.display_tags.size > 0 %}

  <div class="tag-category-list" style="margin-bottom: 60px;">
    <ul class="p-0 m-0">
      {% for tag in site.display_tags %}
        <li>
          <i class="fa-solid fa-hashtag fa-sm"></i> <a href="{{ tag | slugify | prepend: '/blog/tag/' | relative_url }}">{{ tag }}</a>
        </li>
        {% unless forloop.last %}
          <p>&bull;</p>
        {% endunless %}
      {% endfor %}
    </ul>
  </div>

{% endif %}

<div class="d-flex justify-content-center align-items-center mb-4" style="margin-top: 40px;">
  
  <a href="https://www.igsb.uni-bonn.de/en" target="_blank" class="mx-4">
    <img src="{{ site.baseurl }}/assets/img/logo-IGSB.jpg" alt="Institute for Genomic Statistics and Bioinformatics" style="max-height: 80px; width: auto;">
  </a>

  <a href="https://www.ukbonn.de/" target="_blank" class="mx-4">
    <img src="{{ site.baseurl }}/assets/img/logo-UKB.svg" alt="Universitätsklinikums Bonn" style="max-height: 80px; width: auto;">
  </a>

</div>
