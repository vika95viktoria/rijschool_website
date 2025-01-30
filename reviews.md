---
layout: reviews
title: Reviews
background: grey
cloudcannon_editable: true
---

<section class="reviews-section py-6 mt-6">
  <div class="container">
    <h2 class="text-center mb-4">My students say:</h2>
    
{% assign total_reviews = site.data.sitetext.reviews.size %}
{% assign num_of_carousel = total_reviews | divided_by: 3 %}
{% assign remainder = total_reviews | modulo: 3 %}
{%- if remainder == 0 -%}
{% assign num_of_carousel = num_of_carousel | minus: 1 %}
{%- endif -%}

<div id="reviewCarousel" class="carousel slide mb-5" data-ride="carousel">
      <!-- Carousel Indicators (the dots below) -->
      <div class="carousel-indicators">
      {% for i in (0..num_of_carousel) %}
       {%- if i == 0 -%}
       <button type="button" data-bs-target="#reviewCarousel" data-bs-slide-to="0" class="active" aria-current="true" ></button>
        {%- else -%}
        <button type="button" data-bs-target="#reviewCarousel" data-bs-slide-to="{{i}}" ></button>
        {%- endif -%}
      {% endfor %}
      </div>

      
      <!-- Carousel Inner -->
      <div class="carousel-inner">
      {% for i in (0..num_of_carousel) %}
      
      {%- if i == 0 -%}
       <div class="carousel-item active">
          <div class="row justify-content-center">
          
          {% for j in (0..2) %}
          {% assign review = site.data.sitetext.reviews[j] %}
          <div class="col-md-3 col-sm-6 ">
              <div class="review-card">
                <div class="review-header">
                  <div>
                    <h5 class="review-author">{{review.author}}</h5>
                  </div>
                </div>
                <div class="review-stars">
                {% for k in (1..review.num_of_stars) %}
                <i class="bi bi-star-fill"></i>
                {% endfor %}
                </div>
                <div class="review-text">
                  <p>
                    {{review.text}}
                  </p>
                </div>
                <div class="review-footer">
                  <img src="assets/img/google_icon.webp" alt="Google icon" class="google-icon">
                  <a href="{{review.link}}" target="_blank"><span>Posted on Google</span></a>
                </div>
              </div>
            </div>
          {% endfor %}
            
       {%- else -%}
      
      <div class="carousel-item ">
          <div class="row justify-content-center">
          
          {% assign lower_bound = i | times: 3 %}
          {% assign upper_bound = lower_bound | plus: 2 %}
          {%- if upper_bound > total_reviews -%}
          {% assign upper_bound = total_reviews | minus: 1 %}
          {%- endif -%}
          {% for j in (lower_bound..upper_bound) %}
          {% assign review = site.data.sitetext.reviews[j] %}
          <div class="col-md-3 col-sm-6 ">
              <div class="review-card">
                <div class="review-header">
                  <div>
                    <h5 class="review-author">{{review.author}}</h5>
                  </div>
                </div>
                <div class="review-stars">
                {% for k in (1..review.num_of_stars) %}
                <i class="bi bi-star-fill"></i>
                {% endfor %}
                </div>
                <div class="review-text">
                  <p>
                    {{review.text}}
                  </p>
                </div>
                <div class="review-footer">
                  <img src="assets/img/google_icon.webp" alt="Google icon" class="google-icon">
                  <a href="{{review.link}}" target="_blank"><span>Posted on Google</span></a>
                </div>
              </div>
            </div>
          {% endfor %}
          
          
          
           {%- endif -%}
           
          </div> <!-- row -->
       
        </div> <!-- carousel-item -->
      {% endfor %}
      
      </div> <!-- carousel-inner -->
      
       <!-- Carousel Controls -->
      <button class="carousel-control-prev" type="button" data-bs-target="#reviewCarousel" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
      <button class="carousel-control-next" type="button" data-bs-target="#reviewCarousel" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
</div>

</div>
</section>