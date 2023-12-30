<template>
  <div class="mini-card">
    <div class="frame">
      <div class="title">{{ title }}</div>
      <a class="read-more">Read more</a>
    </div>
  </div>
</template>
<script>
import './mini-card.scss'

export default {
  name: 'MiniCard',
  props: {
    title: { type: String, default: '' },
  },
}
</script>
