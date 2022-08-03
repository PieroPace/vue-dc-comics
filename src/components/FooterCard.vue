<template>
  <section class="card-section">
    <div class="container">
      <ul>
        <CardItem 
        v-for="(card, index) in cards"
        :key="index"
        :title="card.title"
        :url="card.url"
        :imgUrl="card.img"
        />
      </ul>
    </div>
  </section>
</template>

<script>
import CardItem from './CardItem.vue';

export default {
  name: "FooterCard",
  components: {
    CardItem,
  },
  data() {
    return {
      cards: [
        {
          title: "Digital Comics",
          url: "#",
          img: require("../assets/img/buy-comics-digital-comics.png")
        },
        {
          title: "DC Merchandise",
          url: "#",
          img: require("../assets/img/buy-comics-merchandise.png")
        },
        {
          title: "Subscriptions",
          url: "#",
          img: require("../assets/img/buy-comics-subscriptions.png")
        },
        {
          title: "Comic Shop Locator",
          url: "#",
          img: require("../assets/img/buy-comics-shop-locator.png")
        },
        {
          title: "DC Power Visa",
          url: "#",
          img: require("../assets/img/buy-dc-power-visa.svg")
        },
      ],
    }
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/style.scss";

.card-section {
  background-color: $brand-font-color;
  padding: 2.5em;
  ul {
    @include flex(center, center);
    gap: 1em;
  }
}
</style>
