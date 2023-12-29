<template>
  <div class="testimonial-card">
    <figure>
      <blockquote>
        <div class="image-wrapper" style="justify-content: flex-start;">
          <img class="image" alt="Quote sign 1" src="assets/images/quote_2.svg" />
        </div>
        <p class="quote">Jus Mundi is an indispensable tool to meet the needs of our clients! It is cost-effective and
          gives us access
          to key information to build the winning strategy.</p>
        <div class="image-wrapper" style="justify-content: flex-end;">
          <img class="image" alt="Quote sign 2" src="assets/images/quote_1.svg" />
        </div>
      </blockquote>
      <figcaption>
        <span class="author-name bold">Dietmar W. Prager</span>
        <span class="author-function span"> – Co-Chair of Dechert’s International Arbitration global practice</span>
      </figcaption>
    </figure>
    <div class="all-testimonials">
      <a>All testimonials</a>
    </div>
  </div>
</template>
<script>
export default {
  name: 'TestimonialCard',
}
</script>
<style scoped>
.testimonial-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 888px;
  margin: 38px auto;
  padding: 0 24px 24px;

  & figure {
    margin: 32px 0;
    padding: 16px 24px;

    & blockquote {
      display: flex;
      margin: 0;
      padding: 0 24px;

      .image-wrapper {
        display: flex;
        flex-direction: column;
      }
    }

    & figcaption {
      & span {
        font-family: 'IBM Plex Sans';
        font-size: 16px;
        font-style: normal;
        font-weight: 400;
        line-height: 150%;
        letter-spacing: unset;
        text-transform: none;
        color: var(--primary-text-color);
      }
    }
  }

  .all-testimonials {
    width: 100%;
    text-align: right;
    margin: 0 96px;

    & a:not(:hover) {
      color: var(--secondary-text-color);
    }
  }
}

@media screen and (max-width: 768px) {
  .testimonial-card figure blockquote {
    margin-bottom: 16px;
  }
}
</style>
