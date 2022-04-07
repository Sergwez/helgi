<template>
  <div class="content">
    <Banner />
    <Services />
    <Testimonial />
    <Blog />
  </div>
</template>

<script>
import Banner from "../components/BannerBlock.vue";
import Services from "../components/ServicesBlock.vue";
import Testimonial from "../components/TestimonialBlock.vue";
import Blog from "../components/BlogBlock.vue";

export default {
  name: "HomeView",
  components: {
    Banner,
    Services,
    Testimonial,
    Blog,
  },
};
</script>
<style>
.content {
  width: 100%;
}
</style>
