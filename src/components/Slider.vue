<template>
  <div class="slider">
    <div class="slider__wrapper">
      <div class="slider__racer" :style="{'margin-left': '-'+ (100 * currentSlideIndex)+ '%'}">
        <SliderItem
            :currentSlider="sliderData[currentSlideIndex]"
            :totalSliders="sliderData.length"
            v-for="item in sliderData"
            :key="item.id"
            :itemData="item"
        />
      </div>
      <p class="main__description_text">{{ sliderData[currentSlideIndex].description }}</p>
    </div>
    <div class="slider__btn" @click="nextSlide">
      <div class="arrow">
        <img src="../common/images/arrowBody.png" alt="arrow">
        <img class="arrowEnd" src="../common/images/arrowEnd.png" alt="arrowEnd">
      </div>
    </div>
  </div>
</template>

<script>
import SliderItem from './SliderItem'

export default {
  name: "Slider",
  components: {
    SliderItem
  },
  props: {
    sliderData: {
      type: [],
      default: () => []
    }
  },
  data() {
    return {
      currentSlideIndex: 0
    }
  },
  methods: {
    nextSlide() {
      if (this.currentSlideIndex === this.sliderData.length - 1) {
        this.currentSlideIndex = 0
        return
      }
      this.currentSlideIndex++
    }
  }
}
</script>

<style scoped>

.slider {
  display: flex;
  justify-content: flex-end;
  width: 100%;
  max-height: 80%;
  overflow: hidden;
}

.slider__wrapper {
  max-width: 304px;
  height: 436px;
  overflow: hidden;
  margin: 0 auto;
}

.slider__racer {
  display: flex;
}

.slider__btn {
  position: relative;
  left: 0;
  bottom: 80px;
  border-radius: 50%;
  border: 1px solid #333333;
  width: 40px;
  height: 40px;
  display: flex;
  justify-content: center;
  align-items: center;
  align-self: center;
  z-index: 2;
}

.arrow {
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  z-index: 2;
}

.arrowEnd {
  position: absolute;
  right: 0;
  z-index: 2;
}

.main__description_text {
  position: absolute;
  font-size: 20px;
  line-height: 32px;
  font-family: kinopoiskLight, sans-serif;
  z-index: 21;
  text-align: center;
  max-width: 80%;
  right: 10%;
  bottom: 15%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

@media screen and (max-width: 1302px) and (max-height: 801px) {
  .main__description_text {
    font-size: 14px;
    line-height: 15px;
  }
}
</style>
