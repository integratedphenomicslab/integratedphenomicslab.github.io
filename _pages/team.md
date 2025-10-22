---
layout: page
title: team
permalink: /team/
description: Short Description of Team Members
nav: true
nav_order: 5
horizontal: false
---

{% assign roles_order = "Principal Investigator|Postdoctoral Researcher|PhD Student|Master Student|Research Assistant|Alumni" | split: "|" %}

{% assign all_members = site.data.team %}


{% for role in roles_order %}

  {% assign members_in_role = all_members | where: "role", role %}

  {% if members_in_role.size > 0 %}

    <h2 class="mt-4">{{ role }}</h2>
    <hr>

    <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 row-cols-lg-4 g-4">

      {% for member in members_in_role %}

        <div class="col">
          <div class="card h-100 border-0 text-center">

            <img src="{{ site.baseurl }}{{ member.image_path }}" class="card-img-top rounded-circle p-3 profile-img mx-auto" alt="{{ member.name }}">

            <div class="card-body">

              <h5 class="card-title">{{ member.name }}</h5>

              {% if member.role != "Alumni" %}
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
                      <a href="{{ link.url }}" class="text-decoration-none" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
                    {% endif %}

                  {% endfor %}
                </div>
              {% endif %}

            </div>
          </div>
        </div>
      {% endfor %}

    </div> 
  {% endif %} 
  {% endfor %}
