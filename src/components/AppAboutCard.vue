<template>
  <div class="container">
    <div class="col card mt-4 p-4">
      <div class="title">
        <i class="main-icon me-2" :class="aboutCard.iconClass"></i>
        <h4>{{ aboutCard.title }}</h4>
      </div>
      <p>{{ aboutCard.text }}</p>
    </div>
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
.card {
  border: 1px solid black;
  background-color: #fff;

  .main-icon {
    display: inline-block;
    font-size: 1.8rem;
  }

  h4 {
    display: inline-block;
  }
}
</style>
