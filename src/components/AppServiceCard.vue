<template>
  <div class="card col-4 mt-4 p-4">
    <div class="row row-cols-2 icon-wrapper mb-3">
      <i class="main-icon" :class="serviceCard.iconClass"></i>
      <i class="arrow fas fa-arrow-right text-end"></i>
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

  i {
    color: $brand-primary-clr;

    &.main-icon {
      font-size: 1.8rem;
    }

    &.arrow {
      opacity: 0.7;
    }
  }
}
</style>
