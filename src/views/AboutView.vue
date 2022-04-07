<template>
  <div class="about">
    <h3>Разный размер:</h3>
    <svg class="big">
      <use xlink:href="@/assets/icons/mail.svg"></use>
    </svg>
    <svg class="normal">
      <use xlink:href="@/assets/icons/mail.svg"></use>
    </svg>
    <svg class="small">
      <use xlink:href="@/assets/icons/mail.svg"></use>
    </svg>
    <h3>Цвет:</h3>
    <svg class="normal red">
      <use xlink:href="@/assets/icons/mail.svg"></use>
    </svg>
    <svg class="normal green">
      <use xlink:href="@/assets/icons/mail.svg"></use>
    </svg>
    <svg class="normal blue">
      <use xlink:href="@/assets/icons/mail.svg"></use>
    </svg>
    <h3>Интерактивность:</h3>
    <svg class="normal hover1">
      <use xlink:href="@/assets/icons/mail.svg"></use>
    </svg>
    <svg class="normal hover2">
      <use xlink:href="@/assets/icons/mail.svg"></use>
    </svg>
    <svg class="normal hover3">
      <use xlink:href="@/assets/icons/mail.svg"></use>
    </svg>
  </div>
</template>
<style lang="scss" scoped>
.about {
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  svg {
    transition: 0.3s;
    &.big {
      width: 48px;
      height: 48px;
    }
    &.normal {
      width: 24px;
      height: 24px;
    }
    &.small {
      width: 12px;
      height: 12px;
    }
    &.red {
      fill: red;
    }
    &.green {
      fill: green;
    }
    &.blue {
      fill: blue;
    }
    &.hover1 {
      &:hover {
        fill: red;
      }
    }
    &.hover2 {
      &:hover {
        width: 48px;
        height: 48px;
      }
    }
    &.hover3 {
      &:hover {
        transform: rotate(180deg);
      }
    }
  }
}
</style>
