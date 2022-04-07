<template>
  <div class="wrapper">
    <Header />
    <div class="wrapper__content">
      <router-view />
      <Footer />
    </div>
  </div>
</template>
<script>
import Header from "./components/HeaderBlock.vue";
import Footer from "./components/FooterBlock.vue";

export default {
  components: {
    Header,
    Footer,
  },
};
</script>
<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600&display=swap");
body {
  margin: 0;
}
#app {
  font-family: "Poppins", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.wrapper {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  &__content {
    display: flex;
    flex-direction: column;
    width: 100%;
  }
}
</style>
