<template>
  <div class="circular-icon" :style="getStyle">
    <img :src="src" :alt="alt" />
  </div>
</template>
<script>
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
<style scoped lang="scss">
.circular-icon {
  display: flex;
  align-items: center;
  justify-content: center;
  aspect-ratio: 1/1;
  border-radius: 50%;
  box-shadow: 0px 0px 128px 0px rgba(0, 0, 0, 0.10);

  img {
    width: 60%;
    object-fit: contain;
  }
}
</style>
