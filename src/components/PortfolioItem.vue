<template>
  <section :class="['portfolioItem', color]" :id="title">
    <h2 class="portfolioItemTitle">{{title}}</h2>
    <slot />
  </section>
</template>

<script>
export default {
  props: {
    title: String,
    color: String
  },
}
</script>

<style lang="scss" scoped>
.portfolioItem {
  background-color: #ccc;
  min-height: 600px;
  overflow: hidden;
  position: relative;
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
  position: relative;
  z-index: 1;
}
</style>
