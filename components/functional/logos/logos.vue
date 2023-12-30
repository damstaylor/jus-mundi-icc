<template>
  <div class="logos">
    <div v-for="(item, key) in items" :key="`logo-${key}`" class="img-container">
      <img :src="item.src" :alt="item.alt" />
    </div>
  </div>
</template>
<script>
import './logos.scss'

export default {
  name: 'Logos',
  props: {
    items: { type: Array, default: () => [] },
  },
}
</script>
