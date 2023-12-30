<template>
  <button :class="`button ${variant}`">
    <img v-if="icon" :src="icon" />{{ text }}
  </button>
</template>
<script>
import './button.scss'

export default {
  name: 'Button',
  props: {
    text: { type: String, default: '' },
    icon: { type: String, default: '' },
    variant: { type: String, default: 'primary' },
  },
}
</script>
