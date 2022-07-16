<template>
  <div class="rightBar">
    <p class="rightBar__link">hd.kinopoisk.ru</p>
  </div>
</template>

<script>
export default {
  name: "RightBar"
}
</script>

<style scoped>
.rightBar {
  display: flex;
  justify-content: flex-end;
  align-items: center;
}

.rightBar__link {
  color: #333333;
  font-family: kinopoiskMedium, sans-serif;
  font-size: 14px;
  line-height: 15px;
  transform: rotate(90deg);
  z-index: 2;
  position: relative;
  left: 40px;
}

@media screen and (max-width: 1302px) and (max-height: 801px) {
  .rightBar__link {
    font-size: 12px;
  }
}
</style>
