<template>
  <main class="main-content container-margin side-padding">
    <header>
      <Line />
      <Button text="Try Jus Mundi" :icon="imgPath('ico-arrow_up.svg')" variant="secondary" />
    </header>
    <div class="two-columns">
      <div class="left">
        <CircularIcon :src="imgPath('logo_icc.svg')" alt="ICC logo" size="483px" class="icc-icon" />
        <CircularIcon :src="imgPath('logo_jm.svg')" alt="JM logo" size="187px" bg-color="var(--faded-primary-color)"
          class="jm-icon" />
        <img class="gif-animation" :src="imgPath('case_bg.gif')" alt="Animation" />
      </div>
      <div class="right">
        <div class="text">
          <h1>A Unique Partnership for the Publication of ICC Arbitration Awards</h1>
          <p>The International Chamber of Commerce (ICC) & Jus Mundi have joined forces to make ICC Arbitration Awards and
            related materials freely available to the global legal community.</p>
        </div>
        <Button text="Access ICC Awards" :icon="imgPath('arrow_right.svg')" />
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
  methods: {
    imgPath(filename) {
      return `assets/images/${filename}`
    },
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
    margin-top: -55px;
    /* To be improved */
  }

  .line-container {
    width: 100%;
    display: flex;
    align-items: flex-end;
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

    .left {
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      position: relative;

      .circular-icon {
        position: absolute;
      }

      .icc-icon {
        bottom: 214px;
        left: 30px;
        z-index: 1;
        transform: scale(0);
        animation: scale-up 1s ease-in-out .1s forwards;
        /* Step 1 */

        &:deep() img {
          opacity: 0;
          animation: fade-in .8s ease-in-out 1.11s forwards;
          /* Step 2 */
        }
      }

      .jm-icon {
        bottom: 64px;
        left: 84px;
        z-index: 1;
        opacity: 0;
        animation: fade-in-diagonal .1s ease-in-out 1.91s forwards;
        /* Step 3 */
      }

      .gif-animation {
        width: 478px;
        height: 496px;
        margin-top: auto;
        z-index: 0;
        opacity: 0;
        animation: fade-in .5s ease-out 2.01s forwards;
        /* Step 4 */
      }
    }

    .right {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      margin-right: 57px;
      padding-bottom: 24px;

      .text {
        width: 582px;
        margin-bottom: 93px;

        & h1 {
          opacity: 0;
          animation: fade-in-up .8s ease-in-out 1.11s forwards;
          /* Step 2 */
        }

        & p {
          opacity: 0;
          animation: fade-in .8s ease-in-out 1.11s forwards;
          /* Step 2 */
        }
      }

      .button {
        z-index: 1;
        opacity: 0;
        animation: fade-in .5s ease-out 2.01s forwards;
        /* Step 4 */
      }
    }
  }
}

@keyframes scale-up {
  from {
    transform: scale(0);
  }
  to {
    transform: scale(1);
  }
}

@keyframes fade-in {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes fade-in-up {
  from {
    transform: translateY(30px);
    opacity: 0;
  }
  to {
    transform: translateY(0);
    opacity: 1;
  }
}

@keyframes fade-in-diagonal {
  from {
    transform: translate(-48px, 20px);
    opacity: 0;
  }
  to {
    transform: translate(0, 0);
    opacity: 1;
  }
}
</style>
