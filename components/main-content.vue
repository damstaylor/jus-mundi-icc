<template>
  <main class="main-content">
    <div class="two-columns">
      <div class="left">
        <img class="animation" src="assets/images/case_bg.gif" alt="Animation" />
      </div>
      <div class="right">
        <div class="text">
          <h1>A Unique Partnership for the Publication of ICC Arbitration Awards</h1>
          <p>The International Chamber of Commerce (ICC) & Jus Mundi have joined forces to make ICC Arbitration Awards and
            related materials freely available to the global legal community.</p>
        </div>
        <Button text="Access ICC Awards" icon="assets/images/arrow_right.svg" />
      </div>
    </div>
  </main>
</template>
<script>
export default {
  name: 'MainContent',
  props: {
  },
}
</script>
<style scoped>
.main-content {
  text-align: start;

  & p {
    text-align: inherit;
    margin: 24px 0;
  }

  & header {
    height: 64px;
    display: flex;
    justify-content: end;
  }

  .two-columns {
    display: flex;
    gap: 48px;
  }

  .left {
    margin-top: auto;

    .animation {
      width: 478px;
      height: 496px;
    }
  }

  .right {
    display: flex;
    flex-direction: column;
    align-items: start;
    padding-bottom: 24px;

    .text {
      width: 582px;
      margin-bottom: 70px;
    }
  }
}
</style>
