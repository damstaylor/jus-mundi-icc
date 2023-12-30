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
import './main-content.scss'
import Button from '../../functional/button/button.vue'
import CircularIcon from '../../functional/circular-icon/circular-icon.vue'
import Line from '../../functional/line/line.vue'

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
