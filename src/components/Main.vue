<template>
  <header class="mainArea">
    <h1 class="title">Kame’s Portfolio</h1>
    <p class="skill">html / css / javascript / typescript / react / vue /</p>

    <ul class="nav">
      <li class="navItem"><a href="#About">About</a></li>
      <li class="navItem"><a href="#Works">Works</a></li>
    </ul>
    
  </header>

  <figure
    class="orange"
    v-parallax-speed
    :contentScrollPosition="0"
    styles="transform"
    contentScrollPositionStyleValue="rotate(0deg)"
    :speed="0.02"
    :targetPercentage="0.05"
  ><img src="@/assets/orange.png" /></figure>

  <div class="onrageicons">
    <OrangeIco class="orangeico" v-for="i of 6" :key="i" />
  </div>
</template>

<script>
import OrangeIco from '@/components/icon/OrangeIco.vue'
export default {
  components: {
    OrangeIco
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

<style lang="scss">
.mainArea {
  background-color: #FFF1CD;
  min-height: 600px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.title {
  color: #fff;
  font-size: 40px;
  position: relative;
  z-index: 1;
}

.nav {
  margin-top: 100px;
  position: relative;
  z-index: 1;
  display: flex;
  justify-content: center;
  font-weight: bold;
}

.navItem {
  margin: 0 16px;
  list-style-type: none;
  & a {
    color: #fff;
  }
}

.skill {
  color: #fff;
  font-size: 14px;
  position: relative;
  z-index: 1
}

.orange {
  position: absolute;
  margin: 0 auto;
  top: 15px;
  left: 0;
  right: 0;
}

.orangeico {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  margin: 0 auto;
  z-index: 1;
}

.orangeico:nth-child(1) {
  transform: translate(-330px, 40px) rotate(-40deg);
}
.orangeico:nth-child(2) {
  transform: translate(330px, 40px) rotate(40deg);
}
.orangeico:nth-child(3) {
  transform: translate(-420px, 270px) rotate(-90deg) scale(0.8);
}
.orangeico:nth-child(4) {
  transform: translate(420px, 270px) rotate(90deg) scale(0.8);
}
.orangeico:nth-child(5) {
  transform: translate(-330px, 490px) rotate(-130deg);
}
.orangeico:nth-child(6) {
  transform: translate(330px, 490px) rotate(130deg);
}
</style>