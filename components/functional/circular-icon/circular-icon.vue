<template>
  <div class="circular-icon" :style="getStyle">
    <img :src="src" :alt="alt" />
  </div>
</template>
<script>
import './circular-icon.scss'

export default {
  name: 'CircularIcon',
  props: {
    src: { type: String, default: '' },
    alt: { type: String, default: '' },
    size: { type: String, default: '128px' },
    bgColor: { type: String, default: '#FFFFFF' },
  },
  computed: {
    getStyle() {
      return `width: ${this.size};
              background-color: ${this.bgColor};`
    },
  },
}
</script>
