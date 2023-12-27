<template>
  <footer class="footer container-margin">
    <div class="footer-content">
      <span>Trusted by the best arbitration teams worldwide</span>
      <Logos :items="items" />
    </div>
  </footer>
</template>
<script>

export default {
  name: 'Footer',
  props: {
    items: { type: Array, default: () => [] },
  },
}
</script>
<style scoped>
.footer-content {
  margin: 32px 64px;
}
</style>
