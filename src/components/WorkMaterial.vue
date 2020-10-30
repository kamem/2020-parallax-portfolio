<template>
  <figure class="grape"><img src="@/assets/grape.png" /></figure>

  <GrapeIco 
    v-for="i of 15" 
    :key="i"
    :style="{
      top: randomPositionTop(1000),
      left: randomPosition(2000),
      transform: `scale(${Math.random() + 0.5})`,
      transitionDelay: `${Math.random()}s`
    }"
    class="grapeico"
  />
</template>

<script>
import GrapeIco from '@/components/icon/GrapeIco.vue'
export default {
  components: {
    GrapeIco
  },
  setup() {
    const randomPositionTop = (width) => {
      return Math.random() * width - 100
    }
    const randomPosition = (width) => {
      return Math.random() * width  - width / 2
    }

    return {
      randomPositionTop,
      randomPosition
    }
  }
}
</script>

<style lang="scss">
.on {
  & .grape {
    transform: scale(1);
    opacity: 1;
  }
  & .grapeico {
    opacity: 1;
  }
}
.grape {
  margin: 0 auto;
  position: absolute;
  top: -150px;
  left: 0;
  right: 0;

  opacity: 0;
  transform: scale(0.9);
  transition: all 0.3s;
}
.grapeico {
  position: absolute;

  opacity: 0;
  transition: all 0.3s;
}
</style>