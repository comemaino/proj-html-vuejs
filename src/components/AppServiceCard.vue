<template>
  <div class="card col-4 mt-4 p-5">
    <div class="icon-wrapper row row-cols-2 justify-content-between mb-3">
      <i class="main-icon" :class="serviceCard.iconClass"></i>
      <i class="arrow fas fa-arrow-right text-center"></i>
    </div>
    <h4>{{ serviceCard.title }}</h4>
    <p>{{ serviceCard.text }}</p>
  </div>
</template>

<script>
export default {
  name: "AppServiceCard",
  props: {
    serviceCard: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.card {
  width: 32%;
  background-color: #fff;
  cursor: pointer;

  i {
    line-height: 2.5rem;
    color: $brand-primary-clr;

    &.main-icon {
      font-size: 2rem;
    }

    &.arrow {
      width: 2.5rem;
      height: 2.5rem;
      font-size: 1.2rem;
      border-radius: 50%;
      opacity: 0.7;
    }
  }
  &:hover .arrow {
    background-color: $brand-secondary-clr;
  }
}
</style>
