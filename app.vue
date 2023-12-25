<template>
  <div id="app">
    <div class="content-wrapper">
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
}
</style>
