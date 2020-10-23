<template>
  <section :class="['portfolioItem', color]">
    <h2 class="portfolioItemTitle">{{title}}</h2>
    <slot />
  </section>
</template>

<script>
export default {
  props: {
    title: String,
    color: String
  }
}
</script>

<style lang="scss" scoped>
.portfolioItem {
  background-color: #ccc;
  height: 600px;
  overflow: hidden;
  &.pink {
    background-color: #FFADD4;
  }
  &.purple {
    background-color: #BBA3FF;
  }
}

.portfolioItemTitle {
  margin-top: 40px;
  font-size: 40px;
  font-weight: normal;
  text-align: center;
  color: #fff;
}
</style>
