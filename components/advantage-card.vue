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
export default {
  name: 'AdvantageCard',
  props: {
    imageUrl: { type: String, default: '' },
    title: { type: String, default: '' },
    text: { type: String, default: '' },
  },
}
</script>
<style scoped>
.advantage-card {
  margin: 32px 0;
  max-width: 415px;
  flex: 1;

  & img {
    width: 48px;
    height: 48px;
    margin-bottom: 17px;
  }

  & p {
    font-size: 16px;
    line-height: 24px; /* 150% */
  }
}
</style>