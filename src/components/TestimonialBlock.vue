<template>
  <div class="testimonial">
    <div class="testimonial__content">
      <div class="testimonial__quotes">
        <img src="@/assets/icons/quotes.png" />
      </div>
      <div class="testimonial__text">
        In hac habitasse platea dictumst. Phasellus finibus ipsum enim, non
        pretium massa mattis non. Curabitur ut tempus ex. Nunc dictum est enim,
        consectetur convallis odio mollis tempus!
      </div>
      <div class="testimonial__author">Jim Gordon (GCPD)</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TestimonialBlock",
};
</script>

<style scoped lang="scss">
.testimonial {
  background-color: #353a3f;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  height: 600px;
  background-image: url("@/assets/img/quotes_bg.png");
  background-position: center center;
  background-repeat: no-repeat;
  background-size: 60%;
  @media (min-width: 540px) {
    background-size: 50%;
  }
  @media (min-width: 980px) {
    background-size: auto;
  }
  &__content {
    padding: 0 16px;
    margin-top: -4px;
    @media (min-width: 540px) {
      padding: 0 16px;
    }
    @media (min-width: 980px) {
      padding: 0 6px;
      width: 778px;
    }
  }
  &__quotes {
    margin-bottom: 15px;
    text-align: left;
  }
  &__text {
    color: #fff;
    font-style: italic;
    font-weight: 300;
    font-size: 22px;
    line-height: 38px;
    text-align: left;
    margin-bottom: 72px;
    @media (min-width: 540px) {
      font-size: 28px;
    }
  }
  &__author {
    position: relative;
    text-align: left;
    color: #8c9198;
    font-weight: 500;
    font-size: 20px;
    &::before {
      content: "";
      position: absolute;
      top: -17px;
      width: 60px;
      height: 4px;
      border-radius: 2px;
      background-color: #8c9197;
    }
  }
}
</style>
