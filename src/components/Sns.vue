<template>
  <ul class="sns">
    <li class="sns-item"><a href="http://twitter.com/kamem"><Twitter /></a></li>
    <li class="sns-item"><a href="http://github.com/kamem"><Github /></a></li>
    <li class="sns-item"><a href="http://instagram.com/kamem"><Instagram /></a></li>
  </ul>
</template>

<script>
import Twitter from '@/components/icon/Twitter.vue'
import Github from '@/components/icon/Github.vue'
import Instagram from '@/components/icon/Instagram.vue'

export default {
  components: {
    Twitter,
    Github,
    Instagram
  }
}
</script>

<style lang="scss" scoped>
.sns {
  display: flex;
  justify-content: center;
  list-style-type: none;
  position: relative;
  z-index: 10;
}

.sns-item {
  margin: 0 20px;
}
</style>