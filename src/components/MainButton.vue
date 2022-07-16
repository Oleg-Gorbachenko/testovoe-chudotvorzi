<template>
  <button class="button">
    <p class="button__name">Искать промокод</p>
    <div class="button__arrow">
      <img class="button__arrowBody" src="../common/images/arrowBody.png" alt="arrow">
      <img class="button__arrowEnd" src="../common/images/arrowEnd.png" alt="arrowEnd">
    </div>
  </button>
</template>

<script>
export default {
  name: "MainButton"
}
</script>

<style scoped>
.button {
  z-index: 20;
  display: flex;
  padding: 10px;
  justify-content: space-around;
  align-items: center;
  width: 230px;
  background: #FFFFFF;
  box-shadow: 0 5px 26px rgba(11, 75, 92, 0.0975713);
  border-radius: 8px;
  border: none;
  margin: 40px auto;
}

.button__name {
  font-size: 15px;
  line-height: 18px;
  text-align: center;
  color: #333333;
  font-family: kinopoiskMedium, sans-serif;
}

.button__arrow {
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
}

.button__arrowBody {
  width: 26px;
  height: 2px;
}

.button__arrowEnd {
  position: absolute;
  right: 0;
}

@media screen and (max-width: 1302px) and (max-height: 801px) {
  .button {
    margin: 15px 0;
  }

  .button__name {
    font-size: 13px;
    line-height: 6px;
  }
}
</style>
