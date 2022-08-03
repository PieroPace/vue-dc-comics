<template>
  <footer>
    <FooterCard />
    <FooterLink />
    <FooterSocial />
  </footer>
</template>

<script>
import FooterCard from "./FooterCard.vue";
import FooterLink from "./FooterLink.vue";
import FooterSocial from "./FooterSocial.vue";

export default {
  name: "Footer",
  components: {
    FooterCard,
    FooterLink,
    FooterSocial,
  },
  data() {
    return {};
  },
};
</script>

<style scoped lang="scss">

</style>
