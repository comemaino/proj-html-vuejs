<template>
  <div class="container">
    <div class="card mt-4 p-4">
      <div class="row row-cols-2 icon-wrapper">
        <i class="main-icon" :class="serviceCard.iconClass"></i>
        <i class="fas fa-arrow-right text-end"></i>
      </div>
      <h4>{{ serviceCard.title }}</h4>
      <p>{{ serviceCard.text }}</p>
    </div>
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
.card {
  background-color: #fff;

  .main-icon {
    font-size: 1.8rem;
  }
}
</style>
