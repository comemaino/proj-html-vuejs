<template>
  <section id="results" aria-labelledby="section-title">
    <div class="top-section py-5">
      <div class="container text-center">
        <h5 class="pt-5 mb-4">what are we doing</h5>
        <h2 id="section-title">
          <span class="highlight">Results</span> in Numbers
        </h2>

        <div class="row row-cols-4 py-5">
          <div class="py-5" v-for="(result, index) in results" :key="index">
            <h3>{{ result.amount }}</h3>
            <h6>{{ result.category }}</h6>
          </div>
        </div>
      </div>
    </div>
    <div class="bottom-section py-5">
      <div class="container text-center py-5">
        <div class="row row-cols-5">
          <div class="col" v-for="(logo, index) in logos" :key="index">
            <img
              :src="require('../assets/img/logo-' + logo.imgUrlId + '.png')"
              :alt="logo.imgAlt"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppProjects",

  props: {
    results: Array,
    logos: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
.top-section {
  color: #fff;

  background-image: url(../assets/img/bg-7.jpg);
  background-position: 0 50%;

  h3 {
    font-size: 2rem;
    font-weight: 700;
    color: $brand-primary-clr;
  }

  h6 {
    font-size: 1.2rem;
    text-transform: capitalize;
  }
}

.bottom-section {
  background-color: $dark-section-bg-clr;

  img {
    height: 1.5rem;
    filter: brightness(4);
  }
}
</style>
