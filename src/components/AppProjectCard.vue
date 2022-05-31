<template>
  <div class="container">
    <div class="col card mt-4">
      <img
        :src="require('../assets/img/project-' + projectCard.imgUrl + '.jpg')"
        :alt="projectCard.text"
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
  img {
    filter: brightness(0.4);
    transition: 400ms;
  }

  .text-wrapper {
    color: #fff;
    position: absolute;
    bottom: 0;
    transition: 200ms;

    p {
      opacity: 0;
      transition: 200ms;
    }
  }

  &:hover img {
    filter: blur(2px) brightness(0.4);
  }
  &:hover .text-wrapper {
    bottom: 3rem;
  }
  &:hover .text-wrapper p {
    opacity: 1;
  }
}
</style>
