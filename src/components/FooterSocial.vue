<template>
  <section class="footer-bot">
    <div class="container">
      <div class="sign-up">
        <a href="#">SIGN-UP NOW!</a>
      </div>
      <div class="social-link">
        <ul>
          <li>
            <a href="#">Follow Us</a>
          </li>
          <li>
            <img src="../assets/img/footer-facebook.png" alt="" />
          </li>
          <li>
            <img src="../assets/img/footer-periscope.png" alt="" />
          </li>
          <li>
            <img src="../assets/img/footer-pinterest.png" alt="" />
          </li>
          <li>
            <img src="../assets/img/footer-twitter.png" alt="" />
          </li>
          <li>
            <img src="../assets/img/footer-youtube.png" alt="" />
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "FooterSocial",
};
</script>

<style scoped lang="scss">
@import "../assets/scss/style.scss";

.footer-bot {
  background-color: #303030;
  padding: 2em 0;
  .container {
    @include flex(space-between,center);
    .sign-up {
      width: 50%;
      a {
        padding: 0.8em;
        border: 2px solid $brand-font-color;
        color: white;
      }
    }
    .social-link {
      width: 50%;
      ul {
        @include flex(flex-end,center);
        gap: 2em;
        a {
          text-transform: uppercase;
          font-size: 1.5em;
          color: $brand-font-color;
        }
      }
    }
  }
}
</style>
