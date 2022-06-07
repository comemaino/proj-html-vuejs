<template>
  <div class="col proj-card mt-4">
    <img
      class="text-center"
      :src="require('../assets/img/project-' + projectCard.imgUrlId + '.jpg')"
      :alt="projectCard.title"
    />
    <div class="text-wrapper p-4">
      <h4>{{ projectCard.title }}</h4>
      <p>{{ projectCard.text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppProjectCard",
  props: {
    projectCard: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.proj-card {
  position: relative;
  width: 33%;
  cursor: pointer;

  & * {
    transition: 200ms;
  }

  img {
    width: 100%;
    border-radius: 0.5rem;
    filter: brightness(0.4);
  }

  .text-wrapper {
    color: #fff;
    position: absolute;
    bottom: -4rem;
    z-index: 10;

    p {
      opacity: 0;
    }
  }

  &:hover img {
    filter: blur(2px) brightness(0.4);
  }
  &:hover .text-wrapper {
    bottom: -2rem;
  }
  &:hover .text-wrapper p {
    opacity: 1;
  }
}
</style>
