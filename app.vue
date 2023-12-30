<template>
  <div id="app">
    <div class="content-wrapper">
      <MainContent />
      <SecondContent />
      <Newsfeed :articles="newsfeedArticles" />
      <Footer :items="getLogoAttributes" />
    </div>
  </div>
</template>
<script>
import MainContent from './components/page-sections/main-content.vue'
import SecondContent from './components/page-sections/second-content.vue'
import Newsfeed from './components/page-sections/newsfeed.vue'
import Footer from './components/page-sections/footer.vue'

export default {
  name: 'App',
  components: {
    Footer,
    MainContent,
    Newsfeed,
    SecondContent,
  },
  data() {
    return {
      logos: [
        'dla_piper',
        'curtis',
        'burford',
        'freshfields',
        'shearman',
        'uk-fcdo',
        'foley',
        'evershed',
        'mofa',
        'denton',
        'threecrown',
        'gibson-dunn',
      ],
      newsfeedArticles: [
        { title: 'Corsair becomes the latest airline to pilot ICC AOKpass' },
        { title: 'ICC warns EU vaccine export controls must be rolled back without delay' },
        { title: 'Eduardo Silva Romero talks of advancing diversity, scope of ICC Institute as new Chair' },
        { title: 'ICC/UNICEF: Funding shortfalls and supply chain challenges threaten equitable vaccine distribution' },
        { title: 'ICC Trading Thoughts with Karima-Catherine Goundiam, founder of B2beeMatch' },
        { title: 'Guest blog: Making arbitration work in a down market' },
      ],
    }
  },
  computed: {
    getLogoAttributes() {
      return this.logos.map(str => ({ src: `./assets/logos/${str}.svg`, alt: str }))
    },
  },
}
</script>
<style>
@import url('@/public/assets/css/styles.scss');

#app {
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 32px 0;
}

.content-wrapper {
  width: 100%;
}

@media screen and (max-width: var(--screen-width-xs)) {
  #app {
    margin: 16px 0;
  }
}
</style>
