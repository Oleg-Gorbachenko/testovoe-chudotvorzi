<template>
  <div class="img">
    <div class="counter">{{ currentSlider.id }}/{{ totalSliders }}</div>
    <img :src="require('../common/images/sliderItems/'+currentSlider.img)" alt="img">
  </div>
</template>

<script>
export default {
  name: "SliderItem",
  props: {
    currentSlider: {
      type: Object,
      default: () => {
      }
    },
    totalSliders: {
      default: () => 0
    }
  }
}
</script>

<style scoped>
.img {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.counter {
  height: 55px;
  width: 55px;
  box-shadow: 0 5px 26px rgba(0, 0, 0, 0.1);
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: kinopoiskSemibold, sans-serif;
  margin-bottom: 25px;
  background: #FFFFFF;
  z-index: 2;
}

</style>
