<template>
  <header class="mainArea">
    <h1 class="title">Kame’s Portfolio</h1>
    <p class="skill">html / css / javascript / typescript / react / vue /</p>

    <ul class="nav">
      <li class="navItem"><a href="#About">About</a></li>
      <li class="navItem"><a href="#Works">Works</a></li>
    </ul>
    
  </header>

  <figure class="orange"><img src="@/assets/orange.png" /></figure>
</template>


<script>
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
</style>