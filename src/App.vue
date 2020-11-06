<template>
  <main>
    <article>
      <router-view/>
    </article>
  </main>
</template>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
}
html{
  scroll-behavior: smooth;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
