<template>
  <div class="blog-item">
    <div class="blog-item__img"></div>
    <div class="blog-item__info">
      <div class="blog-item__title">title of a post</div>
      <div class="blog-item__text">
        In hac habitasse platea dictumst. Phasellus finibus ipsum enim, non
        pretium massa mattis non. Curabitur ut tempus ex. Nunc dictum est enim,
        consectetur convallis odio mollis tempus.
      </div>
      <button class="blog-item__btn">Read more</button>
    </div>
  </div>
</template>
<script>
export default {
  name: "BlogBlock",
};
</script>

<style scoped lang="scss">
.blog-item {
  display: flex;
  flex-direction: column;

  @media (min-width: 980px) {
    flex-direction: row;
    align-items: center;
  }
  &:not(&:last-child) {
    margin-bottom: 60px;
  }
  &__img {
    background: #c4c4c4;
    border-radius: 6px;
    width: 100%;
    margin-bottom: 31px;
    aspect-ratio: 1.72 / 1;
    @media (min-width: 980px) {
      margin-bottom: 0;
      min-width: 420px;
      margin-right: 30px;
    }
    @media (min-width: 1378px) {
      margin-right: 48px;
      min-width: 565px;
    }
    @media (min-width: 1440px) {
      margin-right: 80px;
    }
  }
  &__info {
    display: flex;
    flex-direction: column;
    text-align: left;
    width: auto;
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
    line-height: 30px;
    margin-bottom: 31px;
    color: #5a5f65;
    @media (min-width: 1378px) {
      width: 565px;
    }
  }
  &__btn {
    width: 175px;
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
