---
layout: default
title: Contact Us 
permalink: /contact-us/
redirect_from:
  - /contact-me/
  - /contact/
---

<!-- Header Start -->
<div class="container-fluid hero-header bg-light py-5 mb-5">
  <div class="container py-5">
    <div class="row g-5 align-items-center">
      <div class="col-lg-6">
        <h1 class="display-4 mb-3 animated slideInDown">{{ site.contact.title }}</h1>
        <nav aria-label="breadcrumb animated slideInDown">
          <ol class="breadcrumb mb-0">
            <li class="breadcrumb-item"><a href="/">Home</a></li>
            <li class="breadcrumb-item"><a href="#">Pages</a></li>
            <li class="breadcrumb-item active" aria-current="page">{{ site.contact.title }}</li>
          </ol>
        </nav>
      </div>
      <div class="col-lg-6 animated fadeIn">
        <div class="row g-3">
          <div class="col-6 text-end">
            <img class="img-fluid bg-white p-3 w-100" src="img/hero-1.jpg" alt="">
          </div>
          <div class="col-6">
            <img class="img-fluid bg-white p-3 w-100" src="img/hero-2.jpg" alt="">
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
<!-- Header End -->

<!-- Contact Start -->
<div class="container-xxl py-5">
  <div class="container">
    <div class="text-center mx-auto wow fadeInUp" data-wow-delay="0.1s" style="max-width: 500px;">
      <p class="text-primary text-uppercase mb-2">{{ site.contact.title }}</p>
      <h1 class="display-6 mb-5">{{ site.contact.subtitle }}</h1>
    </div>
    <div class="row g-0 justify-content-center">
      <div class="col-lg-8 wow fadeInUp" data-wow-delay="0.1s">
        <p class="text-center mb-4">{{ site.contact.description }}</p>
        <form>
          <div class="row g-3">
            <div class="col-md-6">
              <div class="form-floating">
                <input type="text" class="form-control" id="name" placeholder="Your Name">
                <label for="name">Your Name</label>
              </div>
            </div>
            <div class="col-md-6">
              <div class="form-floating">
                <input type="email" class="form-control" id="email" placeholder="Your Email">
                <label for="email">Your Email</label>
              </div>
            </div>
            <div class="col-12">
              <div class="form-floating">
                <input type="text" class="form-control" id="subject" placeholder="Subject">
                <label for="subject">Subject</label>
              </div>
            </div>
            <div class="col-12">
              <div class="form-floating">
                <textarea class="form-control" placeholder="Leave a message here" id="message" style="height: 200px"></textarea>
                <label for="message">Message</label>
              </div>
            </div>
            <div class="col-12 text-center">
              <button class="btn btn-primary py-3 px-5" type="submit">Send Message</button>
            </div>
          </div>
        </form>
        <div class="mt-4 text-center">
          <p><strong>Email:</strong> {{ site.contact.email }}</p>
          <p><strong>Phone:</strong> {{ site.contact.phone }}</p>
          <p><strong>Address:</strong> {{ site.contact.address }}</p>
        </div>
      </div>
    </div>
  </div>
</div>
<!-- Contact End -->

<!-- Google Map Start -->
<div class="container-xxl py-5 px-0 wow fadeInUp" data-wow-delay="0.1s">
  <iframe class="w-100 mb-n2" style="height: 450px;"
    src="{{ site.contact.map }}"
    frameborder="0" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
</div>
