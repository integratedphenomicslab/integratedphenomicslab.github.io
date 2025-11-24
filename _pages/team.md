---
layout: page
title: TEAM
permalink: /team/
description: Meet the people who makes magic happens
nav: true
nav_order: 5
horizontal: false
---

{% assign team_members = site.data.team %}

{% if team_members %}

  <h2 class="mt-4">所有成員</h2>
  <hr>
  
  <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 row-cols-lg-4 g-4">
  
  {% for member in team_members %} 
  
<div class="col">
      <div class="card h-100 border-0 text-center">

{% if member.profile_url %}
        <a href="{{ site.baseurl }}{{ member.profile_url }}" title="{{ member.name }}'s Profile">
        {% endif %}
        
<img src="{{ site.baseurl }}{{ member.image_path }}" class="card-img-top rounded-circle p-3 profile-img mx-auto" alt="{{ member.name }}">
        
 {% if member.profile_url %}
        </a>
        {% endif %}

 <div class="card-body">

{% if member.profile_url %}
          <a href="{{ site.baseurl }}{{ member.profile_url }}" class="text-decoration-none text-dark" title="{{ member.name }}'s Profile">
          {% endif %}
          
 <h5 class="card-title">{{ member.name }}</h5>
          
{% if member.profile_url %}
          </a>
          {% endif %}

{% if member.role %}
          <p class="card-text text-muted">{{ member.role }}</p>
          {% endif %}
          
 {% if member.links %}
          <div class="people-links mt-2">
          {% for link in member.links %}

{% if link.type == 'email' %}
            <a href="{{ link.url }}" class="text-decoration-none" title="Email"><i class="fas fa-envelope"></i></a>
            {% elsif link.type == 'google-scholar' %}
            <a href="{{ link.url }}" class="text-decoration-none" target="_blank" title="Google Scholar"><i class="fas fa-graduation-cap"></i></a>
            {% elsif link.type == 'github' %}
            <a href="{{ link.url }}" class="text-decoration-none" target="_blank" title="GitHub"><i class="fab fa-github"></i></a>
            {% elsif link.type == 'website' %}
            <a href="{{ link.url }}" class="text-decoration-none" target="_blank" title="Personal Website"><i class="fas fa-globe"></i></a>
            {% elsif link.type == 'linkedin' %}
            <a href="{{ link.url }}" class="text-decoration-none" target="_blank" title="linkedin"><i class="fab fa-linkedin"></i></a>
            {% elsif link.type == 'twitter' %}
            <a href="{{ link.url }}" class="text-decoration-none" target="_blank" title="Twitter"><i class="fab fa-twitter"></i></a>
            {% elsif link.type == 'resume' %}
            <a href="{{ link.url }}" class="text-decoration-none" target="_blank" title="Resume"><i class="far fa-file-alt"></i></a>
            {% endif %}

{% endfor %}
          </div>
          {% endif %}
  
 </div>
      </div>
    </div>
  {% endfor %}
  
  </div>

{% else %}
  <p>目前實驗室成員資料正在更新中。</p>
{% endif %}
