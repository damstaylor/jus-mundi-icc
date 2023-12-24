<template>
  <div id="app">
    <Footer :items="imagePaths" />
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
      ]
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
  height: 100vh;
  max-width: 1308px;
  text-align: center;
  display: flex;
  flex-direction: column;
  margin: auto;
}
</style>
