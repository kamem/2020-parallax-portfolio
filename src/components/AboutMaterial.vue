<template>
  <figure class="apple1"
    v-parallax-speed
    styles="top"
    :speed="0.2"
    contentScrollPosition="#About"
  ><img src="@/assets/apple1.png" /></figure>

  <figure class="apple2"
    v-parallax-speed
    styles="top"
    :speed="-0.3"
    contentScrollPosition="#About"
  ><img src="@/assets/apple2.png" /></figure>

  <AppleIco 
    v-for="i of 7" 
    :key="i"
    :style="{
      top: randomPosition(1000),
      left: randomPosition(2000),
      transform: `scale(${Math.random() + 0.5})`,
    }"
    class="aplleico"

    v-parallax-speed
    styles="top"
    :speed="Math.random() * 2 + 0.5"
    contentScrollPosition="#About"
  />
</template>

<script>
import AppleIco from '@/components/icon/AppleIco.vue'
export default {
  components: {
    AppleIco
  },
  setup() {
    const randomPosition = (width) => {
      return Math.random() * width  - width / 2
    }

    return {
      randomPosition
    }
  }
}
</script>

<style lang="scss" scoped>
.apple1 {
  position: absolute;
  margin: 0 auto;
  top: -100px;
  left: -600px;
  right: 0;
  z-index: 1;
}
.apple2 {
  position: absolute;
  margin: 0 auto;
  top: 200px;
  left: 600px;
  right: 0;
  z-index: 1;
}

.aplleico {
  margin: 0 auto;
  position: absolute;
  left: 0;
  right: 0;
}
</style>