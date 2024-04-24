<template>
  <div class="testimonial-card">
    <figure>
      <blockquote>
        <div class="image-wrapper opening-quote">
          <img class="image" alt="Quote sign 1" src="public/assets/images/quote_2.svg" />
        </div>
        <p class="quote">Jus Mundi is an indispensable tool to meet the needs of our clients! It is cost-effective and
          gives us access
          to key information to build the winning strategy.</p>
        <div class="image-wrapper closing-quote">
          <img class="image" alt="Quote sign 2" src="public/assets/images/quote_1.svg" />
        </div>
      </blockquote>
      <figcaption>
        <span class="author-name bold">Dietmar W. Prager</span>
        <span class="author-function"> – Co-Chair of Dechert’s International Arbitration global practice</span>
      </figcaption>
    </figure>
    <div class="all-testimonials">
      <a>All testimonials</a>
    </div>
  </div>
</template>
<script>
import './testimonial-card.scss'

export default {
  name: 'TestimonialCard',
}
</script>
