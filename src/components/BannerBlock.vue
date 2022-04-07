<template>
  <div class="banner">
    <div class="banner__content">
      <h1 class="banner__title">Title Of The Page</h1>
      <h3 class="banner__subtitle">Subtitle</h3>
      <div class="banner__text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam pharetra
        turpis tristique nisi laoreet gravida. Sed sed orci ut ante pellentesque
        efficitur id ac erat. Morbi metus metus, dictum sed arcu at, interdum
        porttitor erat.
      </div>
      <button class="banner__btn">Button</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "BannerBlock",
};
</script>

<style scoped lang="scss">
.banner {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background-color: #353a3f;
  &__content {
    text-align: left;
    padding: 30px 16px 30px;
    @media (min-width: 540px) {
      padding: 0 30px 30px;
    }
    @media (min-width: 980px) {
      width: 660px;
    }
    @media (min-width: 1378px) {
      width: 810px;
      padding: 0 6px 30px;
    }
  }
  &__title {
    font-weight: 600;
    font-size: 48px;
    text-transform: uppercase;
    color: #fff;
    margin-bottom: -7px;
    position: relative;
    @media (min-width: 540px) {
      font-size: 62px;
    }
    &::before {
      content: "";
      position: absolute;
      width: 60px;
      height: 4px;
      top: -10px;
      border-radius: 2px;
      background-color: #4cb481;
    }
  }
  &__subtitle {
    font-weight: 500;
    font-size: 24px;
    text-transform: uppercase;
    color: #fff;
    margin-bottom: 12px;
    @media (min-width: 540px) {
      font-size: 30px;
    }
  }
  &__text {
    font-weight: 300;
    font-size: 20px;
    line-height: 36px;
    color: rgba(#fff, 0.5);
    margin-bottom: 50px;
    line-height: 28px;
    @media (min-width: 540px) {
      font-size: 22px;
      line-height: 36px;
    }
  }
  &__btn {
    width: 200px;
    height: 60px;
    border-radius: 100px;
    background: #4cb481;
    font-weight: 600;
    font-size: 20px;
    text-transform: uppercase;
    color: #fff;
    border: none;
    cursor: pointer;
    transition: 0.3s;
    &:hover {
      background: rgba(#4cb481, 0.8);
    }
  }
}
</style>
