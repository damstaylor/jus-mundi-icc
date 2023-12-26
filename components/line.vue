<template>
  <div class="line" :style="lineStyle">
  </div>
</template>
<script scoped>
export default {
  name: 'Line',
  props: {
    rotate: { type: String, default: '0' },
    height: { type: String, default: '2px' },
    width: { type: String, default: '24px' },
    color: { type: String, default: '' },
  },
  computed: {
    lineStyle() {
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
<style scoped>
.line {
  background-color: var(--tertiary-color);
}
</style>
