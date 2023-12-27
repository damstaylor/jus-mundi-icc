<template>
  <div class="circular-icon" :style="getStyle">
    <img :src="src" :alt="alt" />
  </div>
</template>
<script scoped>
export default {
  name: 'CircularIcon',
  props: {
    src: { type: String, default: '' },
    alt: { type: String, default: '' },
    size: { type: String, default: '128px' },
    backgroundColor: { type: String, default: '#FFFFFF' },
    opacity: { type: Number, default: 1 },
  },
  computed: {
    getStyle() {
      return `width: ${this.size};
              height: ${this.size};
              background-color: ${this.backgroundColor};
              opacity: ${this.opacity};`
    },
  },
}
</script>
<style scoped>
.circular-icon {
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  box-shadow: 0px 0px 128px 0px rgba(0, 0, 0, 0.10);

  & img {
    width: 60%;
    object-fit: contain;
  }
}
</style>
