<template>
  <header>
    <div class="container">
      <div class="logo">
        <img src="../assets/img/dc-logo.png" />
      </div>
      <ul class="menu-inline">
        <MenuInlineItem
        v-for="(link, index) in links_menu"
        :key="index" 
        :title="link.title"
        :url="link.url"
        :active="link.current"
        @my-event="changeActive(index)"
        />
      </ul>
    </div>
  </header>
</template>

<script>
import MenuInlineItem from './MenuInlineItem.vue';

export default {
  name: "Header",
  components: {
    MenuInlineItem,
  },
  data() {
    return {
      links_menu: [
        {
          title: "Character",
          url: "#",
          current: false
        },
        {
          title: "Comics",
          url: "#",
          current: true
        },
        {
          title: "Movies",
          url: "#",
          current: false
        },
        {
          title: "Tv",
          url: "#",
          current: false
        },
        {
          title: "Games",
          url: "#",
          current: false
        },
        {
          title: "Collectibles",
          url: "#",
          current: false
        },
        {
          title: "Videos",
          url: "#",
          current: false
        },
        {
          title: "Fans",
          url: "#",
          current: false
        },
        {
          title: "News",
          url: "#",
          current: false
        },
        {
          title: "Shop",
          url: "#",
          current: false
        },
      ]
    };
  },
  methods: {
    changeActive: function(index) {
      this.links_menu.forEach((element,indexElement) => {
        if (index == indexElement) {
          element.current = true;
        } else {
          element.current = false;
        }
      });
    }
  }
};


</script>

<style scoped lang="scss">
@import "../assets/scss/style.scss";

.container {
  @include flex(center,center);
  height: $header-height;
  .logo {
    flex-basis: 30%;
    img {
      width: 70px;
    }
  }
  .menu-inline{
    @include flex(center,center);
    height: 100%;
  }
}
</style>
