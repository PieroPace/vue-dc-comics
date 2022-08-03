<template>
  <li @click="$emit('my-event')" :class="(active) ? 'active' : ''">
    <a :href="url">{{ title }}</a>
  </li>
</template>

<script>
export default {
  name: "MenuInlineItem",
  props: ["title", "url", "active"],
};
</script>

<style scoped lang="scss">
@import "../assets/scss/style.scss";

li {
  height: 100%;
  line-height: $header-height;
  a {
    text-transform: uppercase;
    font-weight: bold;
    font-size: 0.8em;
    padding: 1em;
  }
  &.active,
  &:hover {
    position: relative;
    &::after {
      content: "";
      width: 100%;
      height: 3px;
      background-color: $brand-font-color;
      position: absolute;
      top: 98%;
      left: 0;
    }
    a {
      color: $brand-font-color;
    }
  }
}
</style>
