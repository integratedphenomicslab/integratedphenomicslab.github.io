---
layout: about
title: WELCOME
permalink: /
nav: False

selected_papers: false # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: false # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

<div class="header-bar text-center mt-4 mb-5 mx-auto">
  <h1 class="display-4 font-weight-bold">{{ site.title }}</h1>
  
  <div class="d-flex justify-content-center">
      <p class="lead text-muted mt-3" style="max-width: 750px; line-height: 1.6;">
        {{ site.description }}
      </p>
  </div>
</div>
