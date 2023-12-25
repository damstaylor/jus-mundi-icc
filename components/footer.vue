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
}
</script>
<style scoped>
.footer {
  margin: 32px 0;
}
</style>
