<template>
  <footer class="footer max-w side-margin-auto">
    <div class="footer-content">
      <h5>Trusted by the best arbitration teams worldwide</h5>
      <Logos :items="items" />
    </div>
  </footer>
</template>
<script>
import Logos from '../../functional/logos/logos.vue'
import './footer.scss'

export default {
  name: 'Footer',
  components: {
    Logos,
  },
  props: {
    items: { type: Array, default: () => [] },
  },
}
</script>
