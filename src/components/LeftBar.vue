<template>
  <div class="leftBar">
    <div>
      <BurgerMenu/>
    </div>
    <div class="helper">
      <div class="helper__dash"></div>
      <div class="helper__dash"></div>
      <p class="helper__text"><strong>ОЗ</strong> Подсказки</p>
      <div class="helper__dash"></div>
    </div>
    <div class="scroll">
      <div class="scroll__arrow">
        <img class="scroll__arrowBody" src="../common/images/arrowBody.png" alt="arrow">
        <img class="scroll__arrowEnd" src="../common/images/arrowEnd.png" alt="arrowEnd">
      </div>
      <p class="leftBar__desc">Скрольте вниз</p>
    </div>
  </div>
</template>

<script>
import BurgerMenu from './BurgerMenu'

export default {
  components: {
    BurgerMenu,
  },
  name: "LeftBar"
}
</script>

<style scoped>
.leftBar {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  z-index: 2;
  align-items: flex-start;
  align-content: center;
}

.helper__dash {
  color: #333333;
  width: 8px;
  height: 2px;
  border: 1px solid #333333;
  margin-bottom: 50px;
}

.helper__text {
  padding: 5px;
  border-bottom: 1px solid #333333;
  word-spacing: 15px;
  margin: 50px 0;
  font-family: kinopoiskMedium, sans-serif;
}

.scroll {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  transform: rotate(-90deg);
  width: 5px;
}

.leftBar__desc {
  display: flex;
  color: #333333;
  font-size: 14px;
  line-height: 15px;
  font-family: kinopoiskMedium, sans-serif;
  min-width: 150px;
}

.scroll__arrow {
  display: flex;
  align-items: center;
  position: relative;
  transform: rotate(180deg);
  margin: 0 20px;
}

.scroll__arrowBody {
  width: 63px;
  color: #333333;
  height: 2px;
}

.scroll__arrowEnd {
  position: absolute;
  right: 0;
  z-index: 2;
}

@media screen and (max-width: 1302px) and (max-height: 801px) {
  .helper__dash {
    margin: 25px 0;
  }

  .helper__text {
    margin: 25px 0;
    font-size: 12px;
  }

  .scroll__arrow {
    margin: 0 10px;
  }

  .scroll__arrowBody {
    width: 20px;
  }

  .leftBar__desc {
    font-size: 12px;
    line-height: 15px;
  }
}

</style>
