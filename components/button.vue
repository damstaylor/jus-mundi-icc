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
  font-family: Lato;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
  letter-spacing: 2px;
  text-transform: uppercase;
  border: unset;
  display: flex;
  align-items: center;
  justify-content: center;
  min-width: 32px;
  padding: 20px 32px;
  gap: 8px;
  border-radius: 4px;
  box-shadow: 0px 8px 32px 0px rgba(37, 79, 109, 0.24);

  &:hover {
    opacity: .75;
  }

  &:not(:disabled) {
    cursor: pointer;
    
    & img {
      width: 12px;
      height: 12px;
      padding: 6px;
    };
  }

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
