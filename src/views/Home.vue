<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <PortfolioItem title="About" color="pink">
      <About />
      <AboutMaterial />
    </PortfolioItem>
    <PortfolioItem v-parallax-timing :eventTriggerPercentage="0.2" title="Works" color="purple">
      <Thumbnails :items="items" />
      <WorkMaterial />
    </PortfolioItem>
  </div>
</template>

<script>
// @ is an alias to /src
import PortfolioItem from '@/components/PortfolioItem.vue'
import About from '@/components/About.vue'
import AboutMaterial from '@/components/AboutMaterial.vue'
import WorkMaterial from '@/components/WorkMaterial.vue'
import Thumbnails from '@/components/Thumbnails.vue'

export default {
  name: 'Home',
  components: {
    About,
    AboutMaterial,
    WorkMaterial,
    PortfolioItem,
    Thumbnails
  },
  setup() {
    return {
      items: [
        {
          path: '/img/work.jpg',
          url: '#'
        },
        {
          path: '/img/work.jpg',
          url: '#'
        },
        {
          path: '/img/work.jpg',
          url: '#'
        },
        {
          path: '/img/work.jpg',
          url: '#'
        },
        {
          path: '/img/work.jpg',
          url: '#'
        },
        {
          path: '/img/work.jpg',
          url: '#'
        },
        {
          path: '/img/work.jpg',
          url: '#'
        },
        {
          path: '/img/work.jpg',
          url: '#'
        }
      ]
    }
  }
}
</script>
