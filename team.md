---
layout: default
title: Our Team
---

<!-- Header Start -->
<div class="container-fluid hero-header bg-light py-5 mb-5">
  <div class="container py-5">
    <div class="row g-5 align-items-center">
      <div class="col-lg-6">
        <h1 class="display-4 mb-3 animated slideInDown">{{ site.data.team.team_page.title }}</h1>
        <nav aria-label="breadcrumb" class="animated slideInDown">
          <ol class="breadcrumb mb-0">
            <li class="breadcrumb-item"><a href="/">Home</a></li>
            <li class="breadcrumb-item"><a href="/pages">Pages</a></li>
            <li class="breadcrumb-item active" aria-current="page">Our Team</li>
          </ol>
        </nav>
      </div>
      <div class="col-lg-6 animated fadeIn">
        <div class="row g-3">
          {% for img in site.data.team.team_page.hero_images %}
          <div class="col-6 {% if forloop.index0 == 0 %}text-end{% endif %}">
            <img class="img-fluid bg-white p-3 w-100" src="{{ img.src }}" alt="">
          </div>
          {% endfor %}
        </div>
      </div>
    </div>
  </div>
</div>
<!-- Header End -->

<!-- Team Start -->
<div class="container-xxl px-0 py-5">
  <div class="text-center mx-auto mb-5 wow fadeInUp" data-wow-delay="0.1s" style="max-width: 500px;">
    <p class="text-primary text-uppercase mb-2">{{ site.data.team.team_page.subtitle }}</p>
    <h1 class="display-6 mb-0">{{ site.data.team.team_page.title }}</h1>
  </div>
  <div class="row g-0">
    {% for member in site.data.team.team_page.members %}
    <div class="col-lg-6 wow fadeIn" data-wow-delay="{{ member.delay }}">
      <div class="row g-0
        {% if member.layout == 'reverse' %}flex-sm-row-reverse flex-lg-row
        {% elsif member.layout == 'reverse-lg' %}flex-lg-row-reverse
        {% elsif member.layout == 'reverse-sm' %}flex-sm-row-reverse
        {% else %}flex-sm-row{% endif %}">
        <div class="col-sm-6">
          <div class="team-img position-relative">
            <img class="img-fluid" src="{{ member.image }}" alt="{{ member.name }}">
          </div>
        </div>
        <div class="col-sm-6">
          <div class="h-100 p-5 d-flex flex-column justify-content-between">
            <div class="mb-3">
              <h4>{{ member.name }}</h4>
              <span>{{ member.role }}</span>
            </div>
            <p>{{ member.description }}</p>
            <div class="d-flex">
              {% if member.social.facebook %}
              <a class="btn btn-square btn-outline-primary rounded-circle me-2" href="{{ member.social.facebook }}"><i class="fab fa-facebook-f"></i></a>
              {% endif %}
              {% if member.social.twitter %}
              <a class="btn btn-square btn-outline-primary rounded-circle me-2" href="{{ member.social.twitter }}"><i class="fab fa-twitter"></i></a>
              {% endif %}
              {% if member.social.instagram %}
              <a class="btn btn-square btn-outline-primary rounded-circle me-2" href="{{ member.social.instagram }}"><i class="fab fa-instagram"></i></a>
              {% endif %}
            </div>
          </div>
        </div>
      </div>
    </div>
    {% endfor %}
  </div>
</div>
<!-- Team End -->
