<template>
  <li class="thumb">
    <div class="image-container">
      <img :src="src" :alt="series">
    </div>
      <h2> {{ series }} </h2>
  </li>
</template>

<script>
export default {
  name: "Thumb",
  props: ["src", "price", "series", "typeOfElement"]
};
</script>

<style scoped lang="scss">
.thumb {
  width: calc(100% / 6 - 1em);
  color: white;
  .image-container {
    width: 100%;
    height: 250px;
    overflow: hidden;
    img {
      width: 100%;
    }
  }
  h2 {
    font-size: 1em;
    text-transform: uppercase;
    margin: 1em 0;
  }
  
}
</style>
