<template>
  <div class="col _card mt-4 p-4">
    <div class="title">
      <i class="main-icon me-2" :class="aboutCard.iconClass"></i>
      <h4>{{ aboutCard.title }}</h4>
    </div>
    <p class="mb-1">{{ aboutCard.text }}</p>
  </div>
</template>

<script>
export default {
  name: "AppAboutCard",
  props: {
    aboutCard: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

._card {
  .main-icon {
    display: inline-block;
    font-size: 1.8rem;
    color: $brand-primary-clr;
  }

  h4 {
    display: inline-block;
  }

  p {
    color: $light-text-clr;
  }
}
</style>
