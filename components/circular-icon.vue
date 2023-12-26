<template>
  <div class="circular-icon" :class="variant" :style="`opacity: ${opacity};`">
    <img :src="icon" :alt="alt" />
  </div>
</template>
<script scoped>
export default {
  name: 'CircularIcon',
  props: {
    icon: { type: String, default: '' },
    alt: { type: String, default: '' },
    variant: { type: String, default: 'medium' },
    size: { type: String, default: '128px' },
    backgroundColor: { type: String, default: '' },
    opacity: { type: Number, default: 1 },
  },
}
</script>
<style scoped>
.circular-icon {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 128px;
  height: 128px;
  background-color: #FFFFFF;
  border-radius: 50%;
  box-shadow: 0px 0px 128px 0px rgba(0, 0, 0, 0.10);

  & img {
    width: 60%;
    object-fit: contain;
  }

  &.medium {
    width: 167px;
    height: 167px;
  }

  &.large {
    width: 483px;
    height: 483px;
  }
}
</style>
