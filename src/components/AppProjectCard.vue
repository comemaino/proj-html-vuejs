<template>
  <div class="container">
    <div class="col card mt-4">
      <img
        :src="require('../assets/img/project-' + projectCard.imgUrlId + '.jpg')"
        :alt="projectCard.title"
      />
      <div class="text-wrapper p-2">
        <h4>{{ projectCard.title }}</h4>
        <p>{{ projectCard.text }}</p>
      </div>
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
.card {
  & * {
    transition: 200ms;
  }
  img {
    filter: brightness(0.4);
  }

  .text-wrapper {
    color: #fff;
    position: absolute;
    bottom: -1rem;

    p {
      opacity: 0;
    }
  }

  &:hover img {
    filter: blur(2px) brightness(0.4);
  }
  &:hover .text-wrapper {
    bottom: 0;
  }
  &:hover .text-wrapper p {
    opacity: 1;
  }
}
</style>
