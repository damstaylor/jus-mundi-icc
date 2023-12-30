<template>
  <div class="advantage-card">
    <div class="frame">
      <img :src="imageUrl" alt="" />
      <h3>{{ title }}</h3>
      <p>{{ text }}</p>
    </div>
  </div>
</template>
<script>
import './advantage-card.scss';

export default {
  name: 'AdvantageCard',
  props: {
    imageUrl: { type: String, default: '' },
    title: { type: String, default: '' },
    text: { type: String, default: '' },
  },
}
</script>
