<template>
  <footer class="footer">
    <span>Trusted by the best arbitration teams worldwide</span>
    <Logos :items="items" />
  </footer>
</template>
<script>
import Logos from './logos.vue'

export default {
  name: 'Footer',
  props: {
    items: { type: Array, default: () => [] },
  },
  components: {Logos},
}
</script>
<style scoped>
</style>
