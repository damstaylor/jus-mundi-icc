<template>
  <main class="main-content">
    <header>
      <Line />
      <Button text="Try Jus Mundi" icon="assets/images/ico-arrow_up.svg" variant="secondary" />
    </header>
    <div class="two-columns">
      <div class="left">
        <CircularIcon icon="assets/images/logo_icc.svg" variant="large" class="icc-icon" />
        <CircularIcon icon="assets/images/logo_jm.svg" transparent class="jm-icon" />
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
    <footer>
      <div class="gradient-rectangle"></div>
      <div class="line-container">
        <Line rotate="90deg" />
        <Line rotate="45deg" />
      </div>
    </footer>
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
    margin-top: 32px;
  }

  & header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 15px 0;
    margin-bottom: 78px;
  }

  & footer {
    display: flex;
    height: 120px;
    margin-top: -55px; /* To be improved */
  }

  .line-container {
    width: 100%;
    display: flex;
    align-items: end;
    justify-content: space-between;
    padding-bottom: 53px;
  }

  & .gradient-rectangle {
    background: linear-gradient(180deg, rgba(255, 255, 255, 0.00) 0%, #F5F5F5 69.79%);
    position: absolute;
    right: 0;
    width: 100vw;
    height: 120px;
  }

  .two-columns {
    display: flex;
    justify-content: space-between;
    gap: 48px;
  }

  .left {
    display: flex;
    flex-direction: column;
    align-items: end;
    position: relative;

    .animation {
      width: 478px;
      height: 496px;
      margin-top: auto;
    }

    .circular-icon {
      position: absolute;
    }

    .icc-icon {
      top: -152px;
      left: 0;
    }

    .jm-icon {
      bottom: 72px;
      left: 0;
    }
  }

  .right {
    display: flex;
    flex-direction: column;
    align-items: start;
    margin-right: 57px;
    padding-bottom: 24px;

    .text {
      width: 582px;
      margin-bottom: 93px;
    }
  }
}
</style>
