<template>
  <button :class="`button ${variant}`">
    <img v-if="icon" :src="icon" />{{ text }}
  </button>
</template>
<script scoped>
export default {
  name: 'Button',
  props: {
    text: { type: String, default: '' },
    icon: { type: String, default: '' },
    variant: { type: String, default: 'primary' },
  },
}
</script>
<style scoped>
.button {
  display: flex;
  align-items: center;
  justify-content: center;

  &.primary {
    color: var(--white);
    background-color: var(--primary-color);
  }

  &.secondary {
    height: 48px;
    color: var(--primary-text-color);
    background-color: var(--primary-bg-color);
    font-weight: 600;
    padding: 16px;
    gap: 16px;
    
    & img {
      width: 16px;
      height: 16px;
      padding: 0;
    }
  }
}
</style>
