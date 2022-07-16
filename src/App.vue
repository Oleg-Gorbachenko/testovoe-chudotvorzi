<template>
  <div class="background">
    <img class="rectangle" src="./common/images/rectangle.png" alt="cloud">
    <div class="container">
      <LeftBar/>
      <Main/>
      <Clouds/>
      <RightBar/>
    </div>
  </div>
</template>

<script>
import Main from '@/components/Main'
import LeftBar from '@/components/LeftBar'
import RightBar from '@/components/RightBar'
import Clouds from '@/components/Clouds'

export default {
  components: {
    Main, LeftBar, RightBar, Clouds,
  },
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  max-height: 100vh;
}

@font-face {
  font-family: 'futuraBold';
  src: url("common/fonts/futura-bold.woff2") format('woff2');
  font-weight: normal;
  font-style: normal;
}

@font-face {
  font-family: 'kinopoiskSemibold';
  src: url("common/fonts/kinopoisk-semibold.woff2") format('woff2');
  font-weight: normal;
  font-style: normal;
}

@font-face {
  font-family: 'kinopoiskMedium';
  src: url("common/fonts/kinopoisk-medium.woff2") format('woff2');
  font-weight: normal;
  font-style: normal;
}

@font-face {
  font-family: 'kinopoiskLight';
  src: url("common/fonts/kinopoisk-light.woff2") format('woff2');
  font-weight: normal;
  font-style: normal;
}

.background {
  background: url("common/images/Sky.png") no-repeat center center;
  background-size: 100% 100%;
}

.rectangle {
  position: absolute;
  top: 0;
  width: 100%;
}

.container {
  position: relative;
  padding: 25px 25px 0 25px;
  display: flex;
  justify-content: space-between;
}

</style>
