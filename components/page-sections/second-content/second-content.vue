<template>
  <div class="second-content max-w side-margin-auto side-padding">
    <TestimonialCard />
    <div class="texts">
      <div class="heading">
        <Line />
        <h1>Why this partnership?</h1>
        <Line />
      </div>
      <div class="ps">
        <p>Throughout its 100-year history, ICC has brought global business together to support an international
          rules-based
          order, including the promotion of global trade and commerce through the work of the ICC International Court of
          Arbitration.</p>
        <p>ICC has partnered with Jus Mundi to provide full public access to all publishable ICC International Court of
          Arbitration awards and related documents made as of 1 January 2019</p>
      </div>
    </div>
    <div class="advantage-cards">
      <AdvantageCard v-for="(adv, idx) in advantages" v-bind="adv" :key="`ac-${idx}`" />
    </div>
  </div>
</template>
<script>
import './second-content.scss'
import AdvantageCard from '../../functional/advantage-card/advantage-card.vue'
import TestimonialCard from '../../functional/testimonial-card/testimonial-card.vue'
import Line from '../../functional/line/line.vue'

export default {
  name: 'SecondContent',
  components: {
    AdvantageCard,
    Line,
    TestimonialCard,
  },
  data() {
    return {
      advantages: [
        {
          imageUrl: 'assets/images/morecontent_icon.svg',
          title: 'More key arbitration content',
          text: 'This unique partnership means you will have access to more key arbitration content to level up your arbitration research.'
        },
        {
          imageUrl: 'assets/images/transparency_icon.svg',
          title: 'More transparency',
          text: 'You will appreciate the increase in transparency in arbitration!'
        },
        {
          imageUrl: 'assets/images/efficiency_icon.svg',
          title: 'More efficiency',
          text: 'Jus Mundi’s AI-powered technology efficiently delivers thorough legal research and due diligence with full confidence.'
        },
      ]
    }
  },
}
</script>
