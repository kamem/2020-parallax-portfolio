<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <PortfolioItem title="About" color="pink">
      <About />
      <AboutMaterial />
    </PortfolioItem>
    <PortfolioItem title="Works" color="purple" />
  </div>
</template>

<script>
// @ is an alias to /src
import PortfolioItem from '@/components/PortfolioItem.vue'
import About from '@/components/About.vue'
import AboutMaterial from '@/components/AboutMaterial.vue'

export default {
  name: 'Home',
  components: {
    About,
    AboutMaterial,
    PortfolioItem
  }
}
</script>
