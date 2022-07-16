<template>
  <div class="main">
    <div class="main__header">
      <img src="../common/images/logo.png" alt="logo">
      <h1 class="main__title">они должны что-то знать</h1>
    </div>
    <Slider :sliderData="sliderItems"/>
    <div class="main__description">
      <MainButton/>
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
        {
          id: 1,
          name: 'img1',
          img: "1.png",
          description: 'Для примера мы показали вам его лицо. В первой серии он прячется в подвале за мониторами, и пусть борода не собьёт вас с толку. Найдите героя и нажмите на паузу — ему не терпится отдать вам промокод.'
        },
        {
          id: 2,
          name: 'img2',
          img: "2.png",
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aperiam architecto aut beatae deleniti dolorum eius, eos esse explicabo, laudantium odio odit placeat porro!'
        },
        {
          id: 3,
          name: 'img3',
          img: "3.png",
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aperiam architecto aut beatae deleniti dolorum eius, eos esse explicabo'
        },
        {
          id: 4,
          name: 'img4',
          img: "4.png",
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aperiam architecto aut beatae deleniti dolorum eius'
        },
        {
          id: 5,
          name: 'img5',
          img: "5.png",
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aperiam architecto aut beatae'
        },
        {
          id: 6,
          name: 'img6',
          img: "6.png",
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aperiam architecto aut beatae deleniti dolorum eius, eos esse explicabo, laudantium odio odit placeat porro'
        },
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
}

</style>
