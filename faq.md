---
layout: page
title: FAQ
background: grey
cloudcannon_editable: true
---
<!-- Page-specific style -->
<style>
  /* Only apply to links inside #my-page-content */
  #faq a {
    color: black; /* Your desired color */
    text-decoration: underline; /* Optional */
  }
</style>

<section class="faq-section py-5">
  <div class="container text-center mb-4">
    <h2 class="faq-title">Here you can find answers to our most commonly asked questions about driving lessons.</h2>
  </div>

  <div class="container">
    <!-- FAQ Item 1 -->
    <div class="faq-item shadow-sm">
      <button class="faq-question" type="button">
        How old do I have to be to start driving lessons?
        <span class="faq-icon">+</span>
      </button>
      <div class="faq-answer">
        <p>
           You can legally start taking driving lessons at 16½ years old. You can take the driving
            test at 17, but you must drive with a supervising driver until you turn 18.
          </p>
      </div>
    </div>

    <!-- FAQ Item 2 -->
    <div class="faq-item shadow-sm">
      <button class="faq-question" type="button">
        How many lessons do I need before I can take my driving test?
        <span class="faq-icon">+</span>
      </button>
      <div class="faq-answer">
        <p>
           The average student requires between 20 and 40 lessons. However, it depends on your pace,
            learning style, and confidence behind the wheel.
          </p>
      </div>
    </div>
    
    <div class="faq-item shadow-sm">
      <button class="faq-question" type="button">
        Can I have lessons in English?
        <span class="faq-icon">+</span>
      </button>
      <div class="faq-answer">
        <p>
           Yes, lessons can be in English or Dutch depending on your preference
          </p>
      </div>
    </div>

    <!-- FAQ Item 3 -->
    <div class="faq-item shadow-sm">
      <button class="faq-question" type="button">
        Can I pay for my lessons in installments?
        <span class="faq-icon">+</span>
      </button>
      <div class="faq-answer">
        <p>
           Yes! We offer the option to pay in installments. Please contact us to discuss the
            available payment plans and terms.
           </p>
      </div>
    </div>

    <!-- FAQ Item 4 -->
    <div class="faq-item shadow-sm">
      <button class="faq-question" type="button">
        Do I need to pass my theory test before starting practical lessons?
        <span class="faq-icon">+</span>
      </button>
      <div class="faq-answer">
        <p>
 You can begin driving lessons without having passed the theory exam. However, you must
            have your theory certificate before you can book and take the practical test.
      
        </p>
      </div>
    </div>

    <!-- (Optional) Add more FAQ items as needed -->

    <div class="text-center mt-4">
      <p class="faq-footer">
        If you have more questions just call us or send a message and we would be happy to help      </p>
        <a href="https://wa.me/375293760300" target="_blank" class="btn btn-success">
  Chat via WhatsApp
</a>

    </div>
  </div>
</section>

<!-- FAQ Toggle Script -->
<script>
  document.addEventListener('DOMContentLoaded', function () {
    const faqQuestions = document.querySelectorAll('.faq-question');

    faqQuestions.forEach(function (button) {
      button.addEventListener('click', function () {
        const answer = button.nextElementSibling;
        const icon = button.querySelector('.faq-icon');
        
        // Toggle the answer's visibility
        answer.classList.toggle('open');
        
        // Toggle icon (e.g. plus -> minus)
        if (icon.textContent === '+') {
          icon.textContent = '–';
        } else {
          icon.textContent = '+';
        }
      });
    });
  });
</script>
