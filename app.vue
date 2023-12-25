<template>
  <div id="app">
    <div class="content-wrapper">
      <Newsfeed :articles="newsfeedArticles" />
      <Footer :items="imagePaths" />
    </div>
  </div>
</template>
<script>
export default {
  name: 'App',
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
    imagePaths() {
      return this.logos.map(str => ({ src: `./assets/logos/${str}.svg`, alt: str }))
    },
  },
}
</script>
<style>
@import url('@/public/assets/css/styles.css');

#app {
  height: 100%;
  max-width: 1308px;
  margin: auto;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.content-wrapper {
  width: 100%;
  height: 100%;
}
</style>
