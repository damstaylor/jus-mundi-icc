<template>
  <main class="main-content max-w side-margin-auto side-padding">
    <header>
      <Line />
      <Button text="Try Jus Mundi" :icon="imgPath('ico-arrow_up.svg')" variant="secondary" />
    </header>
    <div class="two-columns">
      <div class="left">
        <CircularIcon :src="imgPath('logo_icc.svg')" alt="ICC logo" size="483px" class="icc-icon" />
        <CircularIcon :src="imgPath('logo_jm.svg')" alt="JM logo" size="187px" bg-color="var(--faded-primary-bg-color)"
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
import Button from '../functional/button.vue'
import CircularIcon from '../functional/circular-icon.vue'
import Line from '../functional/line.vue'

export default {
  name: 'MainContent',
  components: {
    Button,
    CircularIcon,
    Line,
  }, 
  methods: {
    imgPath(filename) {
      return `assets/images/${filename}`
    },
  },
}
</script>
<style scoped lang="scss">
@import '../public/assets/css/animations.scss';

.main-content {
  text-align: start;

  p {
    text-align: inherit;
    margin-top: 32px;
  }

  header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 15px 0;
    margin-bottom: 78px;
  }

  footer {
    display: flex;
    height: 120px;
    margin-top: -55px;
  }

  .line-container {
    width: 100%;
    display: flex;
    align-items: flex-end;
    justify-content: space-between;
    padding-bottom: 53px;
  }

  .gradient-rectangle {
    background: linear-gradient(180deg, rgba(255, 255, 255, 0.00) 0%, #F5F5F5 69.79%);
    position: absolute;
    right: 0;
    width: 100vw;
    height: inherit;
  }

  .two-columns {
    display: flex;
    justify-content: space-between;
    gap: 48px;

    .left {
      flex: 1;
      display: flex;
      justify-content: center;
      position: relative;

      .circular-icon {
        position: absolute;
      }

      .icc-icon {
        top: -133px;
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
        top: 313px;
        left: 84px;
        z-index: 1;
        opacity: 0;
        animation: fade-in-diagonal .1s ease-in-out 1.91s forwards;
        /* Step 3 */
      }

      .gif-animation {
        width: 100%;
        max-width: 478px;
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
      margin: 0 16px;
      padding-bottom: 24px;
      flex: 1;

      .text {
        margin-bottom: 93px;

        h1 {
          opacity: 0;
          animation: fade-in-up .8s ease-in-out 1.11s forwards;
          /* Step 2 */
        }

        p {
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

@media screen and (max-width: 1440px) {
  .main-content .text {
    max-width: 582px;
  }
}

@media screen and (max-width: 1280px) {
  .main-content .two-columns {
    gap: 24px;

    .left {
      .jm-icon {
        top: 190px;
        left: 50px;
      }

      .icc-icon {
        width: 350px !important;
      }
    }
  }
}

@media screen and (max-width: 1024px) {
  .main-content .two-columns .left {
    .icc-icon {
      width: 250px !important;
      top: -80px;
      left: 0px;
    }

    .jm-icon {
      width: 130px !important;
      top: 100px;
    }
  }
}

@media screen and (max-width: 768px) {
  .main-content {
    text-align: center;

    .two-columns {
      flex-direction: column;

      .left {
        .jm-icon {
          top: 190px;
          left: 50px;
        }

        .icc-icon {
          width: 350px !important;
        }
      }

      .right {
        align-items: center;
        margin: 0;

        .text {
          margin-bottom: 48px;
        }
      }
    }
  }
}

@media screen and (max-width: 640px) {
  .main-content .two-columns .left {
    .icc-icon {
      width: 250px !important;
    }

    .jm-icon {
      top: 150px;
    }
  }
}
</style>
