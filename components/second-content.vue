<template>
  <div class="second-content">
    <TestimonialCard />
    <div class="texts">
      <div class="heading">
        <div class="line" />
        <h1>Why this partnership?</h1>
        <div class="line" />
      </div>
      <section class="ps">
        <p>Throughout its 100-year history, ICC has brought global business together to support an international
          rules-based
          order, including the promotion of global trade and commerce through the work of the ICC International Court of
          Arbitration.</p>
        <p>ICC has partnered with Jus Mundi to provide full public access to all publishable ICC International Court of
          Arbitration awards and related documents made as of 1 January 2019</p>
      </section>
    </div>
  </div>
</template>
<script>
export default {
  name: 'SecondContent',
  props: {
  },
}
</script>
<style scoped>
.second-content {
  margin-top: 38px;
  margin-bottom: 32px;

  & section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    max-width: 862px;
    margin: auto;

    & p {
      margin-bottom: 32px;
    }
  }

  .heading {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 32px;

    .line {
      background-color: var(--tertiary-color);
      height: 2px;
      width: 24px;
    }
  }
}
</style>
