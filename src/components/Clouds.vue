<template>
  <div>
    <img class="cloud" src="../common/images/cloud.png" alt="cloud">
    <img class="cloud1" src="../common/images/cloud.png" alt="cloud">
    <img class="cloud2" src="../common/images/cloud.png" alt="cloud">
    <img class="cloud3" src="../common/images/cloud.png" alt="cloud">
    <img class="cloud4" src="../common/images/cloud.png" alt="cloud">
    <img class="cloud5" src="../common/images/cloud.png" alt="cloud">
    <img class="cloud6" src="../common/images/cloud.png" alt="cloud">
    <img class="cloud7" src="../common/images/cloud.png" alt="cloud">
  </div>
</template>

<script>
export default {
  name: "Clouds"
}
</script>

<style scoped>

.cloud {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 60%;
  width: 50%;
}

.cloud1 {
  position: absolute;
  bottom: 0;
  left: 30%;
  z-index: 1;
  height: 45%;
}

.cloud2 {
  position: absolute;
  bottom: 0;
  left: 30%;
  z-index: 1;
  height: 45%;
}

.cloud3 {
  position: absolute;
  bottom: 0;
  right: 180px;
  z-index: 1;
  height: 45%;
  width: 50%;
}

.cloud4 {
  position: absolute;
  top: 0;
  left: 50%;
  z-index: 1;
  height: 40%;
  width: 50%;
  transform: rotate(180deg);
}

.cloud5 {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1;
  height: 40%;
  width: 50%;
  transform: rotate(180deg);
}

.cloud6 {
  position: absolute;
  top: 0;
  left: 25%;
  z-index: 1;
  height: 40%;
  width: 50%;
  transform: rotate(180deg);
}

.cloud7 {
  position: absolute;
  bottom: 0;
  right: 0;
  z-index: 1;
  height: 50%;
  width: 50%;
}

</style>
