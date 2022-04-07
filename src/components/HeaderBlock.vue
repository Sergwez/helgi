<template>
  <BurgerMenu @toggle-menu="isOpen = $event" />
  <div class="header" :class="isOpen ? 'is-open' : ''">
    <div class="header__content">
      <div class="header__logo">SDS</div>
      <hr class="header__hr" />
      <div class="header__menu"><MenuBar /></div>
      <hr class="header__hr" />
      <div class="header__search">
        <img src="@/assets/icons/search.png" />
      </div>
    </div>
  </div>
</template>

<script>
import MenuBar from "../components/MenuBar.vue";
import BurgerMenu from "../components/BurgerMenu.vue";

export default {
  name: "HeaderBlock",
  components: {
    MenuBar,
    BurgerMenu,
  },
  data() {
    return {
      isOpen: false,
    };
  },
};
</script>

<style scoped lang="scss">
.header {
  min-width: 120px;
  padding: 39px 0 0;
  box-sizing: border-box;
  position: fixed;
  top: 0;
  bottom: 0;
  transition: 0.3s;
  z-index: 1;
  height: 100%;
  width: 100%;
  background-color: transparent;
  left: -100%;
  box-sizing: border-box;
  @media (min-width: 540px) {
    min-width: 140px;
    padding: 39px 30px 0;
    display: flex;
    height: auto;
    background-color: #282d31;
    width: auto;
    min-height: 100%;
    position: static;
  }
  @media (min-width: 980px) {
    min-width: 150px;
  }
  &.is-open {
    background-color: #282d31;
    left: 0;
  }
  &__content {
    display: flex;
    position: fixed;
    width: 100%;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    @media (min-width: 540px) {
      width: auto;
    }
  }
  &__logo {
    font-size: 32px;
    color: #4cb481;
    position: relative;
    margin-bottom: 53px;
    &::before {
      content: "";
      position: absolute;
      bottom: -6px;
      left: 50%;
      margin-left: -13px;
      width: 25px;
      height: 4px;
      border-radius: 2px;
      background-color: #4cb481;
    }
  }
  &__hr {
    background: #3e4146;
    width: 100%;
    height: 2px;
    border: none;
    margin-bottom: 35px;
  }
  &__menu {
    width: 100%;
    display: flex;
    text-align: center;
    flex-direction: column;
    align-items: center;
    margin-bottom: 16px;
  }
  &__search {
    margin-top: 14px;
  }
}
</style>
