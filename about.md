---
layout: default
title: ABOUT US
permalink: /about-us/
redirect_from:
  - /about/
  - /about-me/
---
    
<!-- Header Start -->
<div class="container-fluid hero-header bg-light py-5 mb-5">
        <div class="container py-5">
            <div class="row g-5 align-items-center">
                <div class="col-lg-6">
                    <h1 class="display-4 mb-3 animated slideInDown">About Us</h1>
                    <nav aria-label="breadcrumb animated slideInDown">
                        <ol class="breadcrumb mb-0">
                            <li class="breadcrumb-item"><a href="#">Home</a></li>
                            <li class="breadcrumb-item"><a href="#">Pages</a></li>
                            <li class="breadcrumb-item active" aria-current="page">About Us</li>
                        </ol>
                    </nav>
                </div>
                <div class="col-lg-6 animated fadeIn">
                    <div class="row g-3">
                        <div class="col-6 text-end">
                            <img class="img-fluid bg-white p-3 w-100" src="/img/hero-1.jpg" alt="">
                        </div>
                        <div class="col-6">
                            <img class="img-fluid bg-white p-3 w-100" src="/img/hero-2.jpg" alt="">
                        </div>
                    </div>
                </div>
            </div>
        </div>
</div>
<!-- Header End -->


<!-- About Start -->
<div class="container-xxl py-5">
  <div class="container">
    <div class="row g-5">
      <div class="col-lg-6 wow fadeInUp" data-wow-delay="0.1s">
        <div class="row g-3 img-twice position-relative h-100">
          {% for img in site.about.images %}
          <div class="col-6 {% if img.position == 'bottom' %}align-self-end{% endif %}">
            <img class="img-fluid bg-light p-3" src="{{ img.src }}" alt="">
          </div>
          {% endfor %}
        </div>
      </div>
      <div class="col-lg-6 wow fadeInUp" data-wow-delay="0.5s">
        <div class="h-100">
          <p class="text-primary text-uppercase mb-2">{{ site.about.subtitle }}</p>
          <h1 class="display-6 mb-4">{{ site.about.title }}</h1>
          {% for desc in site.about.description %}
          <p>{{ desc }}</p>
          {% endfor %}
          <div class="row g-2 mb-4">
            {% for feature in site.about.features %}
            <div class="col-sm-6">
              <i class="fa fa-check text-primary me-3"></i>{{ feature }}
            </div>
            {% endfor %}
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
<!-- About End -->



<!-- Facts Start -->
{% include facts.html %}
<!-- Facts End -->

{% include team.html %}

<!-- Team End -->
