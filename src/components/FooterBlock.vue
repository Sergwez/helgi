<template>
  <div class="footer">
    <div class="footer__content">
      <div class="footer__info">
        <div class="footer__menu">
          <MenuBar />
        </div>
        <div class="footer__copyright">(c) 2018 NAME. All rights reserved.</div>
      </div>
      <div class="footer__links">
        <a href="" class="facebook">
          <img src="@/assets/icons/facebook.png" />
        </a>
        <a href="" class="twitter">
          <img src="@/assets/icons/twitter.png" />
        </a>
        <a href="" class="instagram">
          <img src="@/assets/icons/instagram.png" />
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import MenuBar from "../components/MenuBar.vue";

export default {
  name: "FooterBlock",
  components: {
    MenuBar,
  },
};
</script>

<style scoped lang="scss">
.footer {
  background: #353a3e;
  display: flex;
  flex-direction: row;
  justify-content: center;
  @media (min-width: 980px) {
    height: 220px;
  }
  &__content {
    display: flex;
    flex-direction: column-reverse;
    align-items: center;
    margin: 30px 0 24px;
    box-sizing: border-box;
    @media (min-width: 980px) {
      margin: 68px 24px 0;
      height: 80px;
      width: 100%;
      flex-direction: row;
      justify-content: space-between;
    }
    @media (min-width: 1378px) {
      width: 1210px;
      margin: 68px 0 0;
    }
  }
  &__info {
    display: flex;
    flex-direction: column;
    text-align: center;
    @media (min-width: 980px) {
      text-align: left;
    }
  }
  &__menu {
    margin-bottom: 10px;
    display: flex;
    flex-direction: column;
    @media (min-width: 980px) {
      display: block;
    }
  }
  &__copyright {
    color: rgba(#fff, 0.3);
    letter-spacing: 0.02em;
    font-weight: 300;
    font-size: 16px;
  }
  &__links {
    margin-bottom: 24px;
    @media (min-width: 980px) {
      margin-bottom: 0;
    }
    .facebook {
      margin-right: 33px;
    }
    .twitter {
      margin-right: 30px;
    }
  }
}
</style>
