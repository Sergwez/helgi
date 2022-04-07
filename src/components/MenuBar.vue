<template>
  <a class="menu-item" href="#"> Work </a>
  <a class="menu-item" href="#"> About </a>
  <a class="menu-item" href="#"> Services </a>
  <a class="menu-item" href="#"> Blog </a>
  <a class="menu-item" href="#"> Contact </a>
</template>

<script>
export default {
  name: "MenuBar",
};
</script>

<style scoped lang="scss">
.menu-item {
  text-transform: uppercase;
  font-weight: 600;
  font-size: 16px;
  line-height: 38px;
  color: rgba(#fff, 0.5);
  text-decoration: none;
  margin-bottom: 13px;
  transition: 0.3s;
  &:hover {
    color: #fff;
  }
  .footer & {
    margin-bottom: 0;
    @media (min-width: 980px) {
      margin-right: 47px;
      font-size: 18px;
    }
  }
}
</style>
