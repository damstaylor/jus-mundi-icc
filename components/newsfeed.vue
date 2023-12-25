<template>
  <div class="newsfeed">
    <div class="header">
      <h4>Newsfeed</h4>
      <h2>ICC International Court of Arbitration News & Links</h2>
    </div>
    <div class="slider-container">
      <div class="slider">
        <div class="mini-cards">
          <MiniCard v-for="article in articles" :title="article.title" />
        </div>
      </div>
      <div class="read-all-news">
        <a>Read all news</a>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Newsfeed',
  props: {
    articles: { type: Array, default: () => [] },
  },
}
</script>
<style scoped>
.newsfeed {
  background-color: var(--secondary-bg-color);
  padding: 32px 0;

  .slider-container {
    margin: 16px 0;

    .slider {
      display: flex;
      margin: 14px 0;
      padding: 64px 0;
      overflow: scroll;
      position: relative;
      white-space: nowrap;

      /* Hide scrollbar */
      &::-webkit-scrollbar {
        width: 0px;
      }

      .mini-cards {
        display: flex;
        margin: 0 64px;
      }
    }
  }
}
</style>
