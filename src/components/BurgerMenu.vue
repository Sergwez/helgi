<template>
  <div class="burger" :class="isOpen ? 'is-open' : ''" @click="toggleMenu()">
    <div class="burger__line"></div>
    <div class="burger__line"></div>
    <div class="burger__line"></div>
  </div>
</template>

<script>
export default {
  name: "BurgerMenu",
  data() {
    return {
      isOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen;
      this.$emit("toggleMenu", this.isOpen);
    },
  },
};
</script>

<style scoped lang="scss">
.burger {
  position: fixed;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 40px;
  z-index: 2;
  margin: 16px 22px;
  right: 0;
  @media (min-width: 540px) {
    display: none;
  }
  &__line {
    width: 40px;
    height: 4px;
    border-radius: 2px;
    background-color: #4cb481;
    margin-bottom: 6px;
    transition: 0.3s;
    .is-open & {
      background-color: #888b8d;
      &:nth-of-type(1) {
        transform: rotate(225deg);
        margin-bottom: -7px;
      }
      &:nth-of-type(2) {
        opacity: 0;
      }
      &:nth-of-type(3) {
        transform: rotate(-225deg);
        margin-top: -7px;
      }
    }
  }
}
</style>
