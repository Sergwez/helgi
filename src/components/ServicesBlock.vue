<template>
  <div class="services">
    <div class="services__content">
      <div class="services__item">
        <div class="services__img">
          <img src="@/assets/icons/photos.png" />
        </div>
        <div class="services__title">Photos</div>
        <div class="services__text">
          Vestibulum suscipit tortor magna, quis pellentesque arcu volutpat ac.
          Tempus leo erat, sit amet ullamcorper nisl.
        </div>
        <button class="services__btn">Button</button>
      </div>
      <div class="services__item">
        <div class="services__img">
          <img src="@/assets/icons/videos.png" />
        </div>
        <div class="services__title">Videos</div>
        <div class="services__text">
          Vestibulum suscipit tortor magna, quis pellentesque arcu volutpat ac.
          Tempus leo erat, sit amet ullamcorper nisl.
        </div>
        <button class="services__btn">Button</button>
      </div>
      <div class="services__item">
        <div class="services__img">
          <img src="@/assets/icons/downloads.png" />
        </div>
        <div class="services__title">Downloads</div>
        <div class="services__text">
          Vestibulum suscipit tortor magna, quis pellentesque arcu volutpat ac.
          Tempus leo erat, sit amet ullamcorper nisl.
        </div>
        <button class="services__btn">Button</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ServicesBlock",
};
</script>

<style scoped lang="scss">
.services {
  display: flex;
  flex-direction: row;
  justify-content: center;
  &__content {
    display: flex;
    flex-direction: column;
    margin-top: 40px;
    @media (min-width: 920px) {
      margin-top: 0;
      flex-direction: row;
      justify-content: space-between;
    }
    @media (min-width: 1378px) {
      width: 1210px;
    }
  }
  &__item {
    margin: 40px 16px;
    padding-bottom: 30px;
    background-color: #f6f6f6;
    border-radius: 6px;
    @media (min-width: 540px) {
      margin: 40px 30px;
    }
    @media (min-width: 920px) {
      margin: 120px 16px;
      padding-bottom: 61px;
    }
    @media (min-width: 1378px) {
      margin: 120px 0;
      width: 363px;
    }
  }
  &__img {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    border-radius: 50%;
    width: 110px;
    height: 110px;
    margin: -55px auto 43px;
    background: #fff;
  }
  &__title {
    font-weight: 600;
    font-size: 30px;
    text-transform: uppercase;
    color: #353a3f;
    margin-bottom: 13px;
  }
  &__text {
    font-weight: 300;
    font-size: 18px;
    padding: 0 12px;
    line-height: 30px;
    margin-bottom: 31px;
    color: #5a5f65;
    @media (min-width: 540px) {
      padding: 0 20px;
    }
    @media (min-width: 1378px) {
      padding: 0 53px;
    }
  }
  &__btn {
    width: 160px;
    height: 55px;
    border-radius: 100px;
    background: #4cb481;
    font-weight: 600;
    font-size: 18px;
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
