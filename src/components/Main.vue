<template>
  <div class="main">
    <div class="main__header">
      <img src="../common/images/logo.png" alt="logo">
      <h1 class="main__title">они должны что-то знать</h1>
    </div>
    <Slider :sliderData="sliderItems"/>
    <div class="main__description">
      <div class="main__description_block">
        <p class="main__description_text">Для примера мы показали вам его лицо. В первой серии он прячется в подвале за
          мониторами, и пусть борода не
          собьёт вас с толку. Найдите героя и нажмите на паузу — ему не терпится отдать вам промокод.</p>
        <MainButton/>
      </div>
    </div>
    <img class="cloud" src="../common/images/cloud.png" alt="cloud">
  </div>
</template>

<script>
import MainButton from './MainButton'
import Slider from './Slider'

export default {
  components: {
    MainButton, Slider
  },
  name: "Main",
  data() {
    return {
      sliderItems: [
        {id: 1, name: 'img1', img: "1.png"},
        {id: 2, name: 'img2', img: "2.png"},
        {id: 3, name: 'img3', img: "3.png"},
        {id: 4, name: 'img4', img: "4.png"},
        {id: 5, name: 'img5', img: "5.png"},
        {id: 6, name: 'img6', img: "6.png"},
      ]
    }
  },
}
</script>

<style scoped>
.main {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  min-height: 90vh;
  width: 65%;
}

.main__title {
  text-transform: uppercase;
  font-family: futuraBold, sans-serif;
  font-size: 45px;
  color: #FFCC64;
  margin: 30px 0;
}

.main__header {
  display: flex;
  flex-direction: column;
  align-items: center;
  z-index: 2;
}

.main__description {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.main__description_block {
  display: flex;
  flex-direction: column;
  align-items: center;
  position: absolute;
  bottom: 0;
}

.main__description_text {
  position: relative;
  font-size: 20px;
  line-height: 32px;
  font-family: kinopoiskLight, sans-serif;
  z-index: 21;
  text-align: center;
  max-width: 80%;
}

.cloud {
  position: absolute;
  bottom: 0;
  height: 45%;
  left: 10%;
}

@media screen and (max-width: 1302px) and (max-height: 801px) {
  .main__title {
    font-size: 30px;
    margin: 10px 0;
  }

  .main__description_text {
    font-size: 14px;
    line-height: 15px;
  }

  .main__description_block {
    bottom: 50px;
  }
}

</style>
