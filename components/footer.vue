<template>
  <footer class="footer max-w side-margin-auto">
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
<style scoped lang="scss">
.footer-content {
  margin: 32px 64px;
}
</style>
