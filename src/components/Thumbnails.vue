<template>
  <ul class="thumbnails">
    <li class="thumbnail" v-for="item in items" :key="item.path">
      <a :href="item.url"><img :src="item.path" alt=""></a>
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    items: Array
  }
}
</script>

<style lang="scss">
:root {
  --thumbnail-width: 140px;
  --thumbnail-margin: 16px;
  --thumbnail-num: 4;
}
.thumbnails {
  padding: 0 8px;
  margin: 40px auto 0;
  display: flex;
  flex-wrap: wrap;
  max-width: calc(var(--thumbnail-width) * var(--thumbnail-num) + var(--thumbnail-margin) * var(--thumbnail-num));
  justify-content: center;
  position: relative;
  z-index: 1;
}
.thumbnail {
  margin: 0 8px var(--thumbnail-margin);
  width: calc(100% / var(--thumbnail-num) - var(--thumbnail-margin));
  max-width: var(--thumbnail-width);
  list-style-type: none;

  & > a {
    display: block;
    background-color: #fff;
    &:hover {
      opacity: 0.8;
    }
  }
  & img {
    display: block;
    width: 100%;
  }

  @media screen and (max-width: 480px) {
    width: calc(50% - 16px);
    max-width: none;
  }
}
</style>