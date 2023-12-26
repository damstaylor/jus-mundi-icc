<template>
  <div class="mini-card">
    <div class="frame">
      <div class="title">{{ title }}</div>
      <a class="read-more">Read more</a>
    </div>
  </div>
</template>
<script>
export default {
  name: 'MiniCard',
  props: {
    title: { type: String, default: '' },
  },
}
</script>
<style scoped>
.mini-card {
  width: 336px;
  height: 144px;
  margin-right: 24px;
  text-align: start;
  text-wrap: wrap;
  display: flex;
  flex-direction: column;
  background-color: var(--primary-bg-color);
  box-shadow: rgba(44, 43, 46, 0.05) 4px 4px 24px 0px;
  border-radius: 8px;
  font-size: 16px;
  line-height: 24px;
  cursor: pointer;

  .frame {
    display: flex;
    flex-direction: column;
    padding: 16px 24px;
    height: 100%;
    overflow: hidden;
  }

  .title {
    color: var(--secondary-color);
    font-weight: 700;
    letter-spacing: 0;
    margin-bottom: 8px;
  }

  & a.read-more {
    text-transform: none;
    font-weight: 400;
    letter-spacing: 0;
    
    &:hover {
      color: unset;
    }
  }
}
</style>
