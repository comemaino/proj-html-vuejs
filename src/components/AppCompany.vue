<template>
  <section id="about" aria-labelledby="company-section-title">
    <div class="container p-0">
      <div class="row row-cols-2">
        <div class="col">
          <h5>about the network</h5>
          <h2 id="company-section-title" class="my-4">
            <span class="highlight">The</span> Company
          </h2>
          <p>
            For 12 years we have been providing audit and warranty, financial
            advice, taxes and related services to select clients.
          </p>
          <div class="row row-cols-2 mb-5">
            <AppAboutCard
              v-for="(aboutItem, index) in aboutItems"
              :key="index"
              :aboutCard="aboutItem"
            />
          </div>
          <div class="buttons">
            <button class="btn brand-btn me-3">get in touch</button>
            <button class="btn alpha-btn">read more</button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import AppAboutCard from "./AppAboutCard.vue";

export default {
  name: "AppCompany",

  props: {
    services: Array,
    aboutItems: Array,
  },

  components: {
    AppAboutCard,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
#about {
  position: relative;

  color: #fff;
  background-color: $dark-section-bg-clr;
  background-image: url(../assets/img/about-4.jpg);
  background-size: 50%;

  background-position: 100% 50%;
  background-repeat: no-repeat;

  &::before,
  &::after {
    content: "";
    background-size: 100%;
    display: inline-block;
    width: 8rem;
    height: 4rem;
    background-image: url(../assets/img/bullets.png);
    position: absolute;
    left: 50%;
    transform: translate(-50%);
    opacity: 25%;
  }

  &::before {
    top: -5%;
  }

  &::after {
    bottom: -5%;
  }

  p {
    color: $light-text-clr;
  }
}
</style>
