<template>
  <div class="newsfeed">
    <div class="header">
      <h4>Newsfeed</h4>
      <h2>ICC International Court of Arbitration News Links</h2>
    </div>
    <div class="slider-container">
      <div class="slider">
        <div class="mini-cards">
          <MiniCard v-for="(article, idx) in articles" :title="article.title" :key="`mc-${idx}`" />
        </div>
      </div>
      <div class="read-all-news">
        <a>Read all news</a>
      </div>
    </div>
  </div>
</template>
<script>
import './newsfeed.scss'
import MiniCard from '../../functional/mini-card/mini-card.vue'

export default {
  name: 'Newsfeed',
  components: {
    MiniCard,
  },
  props: {
    articles: { type: Array, default: () => [] },
  },
}
</script>
