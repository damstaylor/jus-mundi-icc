<template>
  <div class="line" :style="getStyle">
  </div>
</template>
<script>
import './line.scss'

export default {
  name: 'Line',
  props: {
    rotate: { type: String, default: '0' },
    height: { type: String, default: '2px' },
    width: { type: String, default: '24px' },
    color: { type: String, default: '' },
  },
  computed: {
    getStyle() {
      return `
        height: ${this.height};
        width: ${this.width};
        transform: rotate(${this.rotate});
        ${this.color ? 'background-color: ' + this.color : ''}
      `
    },
  },
}
</script>
