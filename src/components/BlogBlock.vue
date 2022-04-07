<template>
  <div class="blog">
    <div class="blog__content">
      <div class="blog__title">From the blog</div>
      <BlogItem v-for="item in 3" :key="item" />
    </div>
  </div>
</template>

<script>
import BlogItem from "../components/BlogItem.vue";

export default {
  name: "BlogBlock",
  components: {
    BlogItem,
  },
};
</script>

<style scoped lang="scss">
.blog {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 70px;
  @media (min-width: 980px) {
    margin-bottom: 118px;
  }
  &__content {
    box-sizing: border-box;
    padding: 0 16px;
    @media (min-width: 1378px) {
      width: 1210px;
    }
  }
  &__title {
    font-weight: 600;
    font-size: 44px;
    text-transform: uppercase;
    color: #353a3f;
    margin-top: 80px;
    position: relative;
    text-align: left;
    margin-bottom: 64px;
    @media (min-width: 980px) {
      margin-top: 138px;
    }
    &::before {
      content: "";
      position: absolute;
      top: -17px;
      width: 60px;
      height: 4px;
      border-radius: 2px;
      background-color: #4cb481;
    }
  }
}
</style>
