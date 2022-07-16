<template>
  <div class="burger">
    <div class="burger__item"></div>
    <div class="burger__item"></div>
    <div class="burger__item"></div>
  </div>
</template>

<script>
export default {
  name: "BurgerMenu"
}
</script>

<style scoped>
.burger__item {
  color: #333333;
  border: 1px solid #333333;
  width: 18px;
  height: 3px;
  margin-bottom: 3px;
}
</style>
