---
layout: page
title: Rates
custom_field: test
background: grey
trial_lesson_price: 60
trial_lesson_duration: 60
one_lesson_price: 95
one_lesson_duration: 90
cloudcannon_editable: true
---
<section class="page-section">
  <div class="container">
    <h2 class="section-heading text-uppercase">Available packages</h2>

    <div class="table-responsive">
      <table class="table table-custom">
        <thead>
          <tr>
            <th scope="col" class="rounded-top-left">Package</th>
            <th scope="col" class="rounded-top-right">Price</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Trial lesson {{page.trial_lesson_duration}} min</td>
            <td>{{page.trial_lesson_price}} €</td>
          </tr>
          <tr>
            <td>1 lesson {{site.data.sitetext.rates.one_lesson.duration}}</td>
            <td>{{site.data.sitetext.rates.one_lesson.price}}</td>
          </tr>
          <tr>
            <td>5 lessons x {{site.data.sitetext.rates.one_lesson.duration}}</td>
            <td>{{site.data.sitetext.rates.five_lessons.price}}</td>
          </tr>
          <tr>
            <td>10 lesson x {{site.data.sitetext.rates.one_lesson.duration}}</td>
            <td>{{site.data.sitetext.rates.ten_lessons.price}}</td>
          </tr>
           <tr>
            <td>20 lesson x {{site.data.sitetext.rates.one_lesson.duration}}</td>
            <td>{{site.data.sitetext.rates.twenty_lessons.price}}</td>
          </tr>
           <tr>
            <td>30 lesson x {{site.data.sitetext.rates.one_lesson.duration}}</td>
            <td>{{site.data.sitetext.rates.thirty_lessons.price}}</td>
          </tr>
           <tr>
            <td>Practical exam</td>
            <td>{{site.data.sitetext.rates.practical_exam.price}}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</section>