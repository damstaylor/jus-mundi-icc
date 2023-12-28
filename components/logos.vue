<template>
  <div class="logos">
    <div v-for="(item, key) in items" :key="_uid + key" class="img-container">
      <img :src="item.src" :alt="item.alt" />
    </div>
  </div>
</template>
<script scoped>
export default {
  name: 'Logos',
  props: {
    items: { type: Array, default: () => [] },
  },
}
</script>
<style scoped>
.logos {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
  gap: 64px;
  padding: 64px 0;
}

.img-container {
  display: flex;
  justify-content: center;
}

img {
  width: 100%;
  max-width: 165px;
  height: auto;
  object-fit: scale-down;
}
</style>
