<template>
  <dl class="about">
    <dt class="aboutLabel">name</dt>
    <dd class="aboutValue">kamem</dd>
    <dt class="aboutLabel">work</dt>
    <dd class="aboutValue">frontend engineer</dd>
    <dt class="aboutLabel">web</dt>
    <dd class="aboutValue"><a href="https://clover.blue">clover.blue</a></dd>
  </dl>

  <Sns />
</template>


<script>
import Sns from '@/components/Sns.vue'

export default {
  components: {
    Sns,
  }
}
</script>

<style lang="scss" scoped>
</style>

<style lang="scss" scoped>
.about {
  display: flex;
  flex-wrap: wrap;
  color: #fff;
  line-height: 2;
}
.aboutLabel {
  width: 50%;
  text-align: right;
  &:after {
    content: ': ';
    margin-right: 8px;
  }
}
.aboutValue {
  width: 50%;
  text-align: left;
  & > a {
    color: #fff;
  }
}
</style>