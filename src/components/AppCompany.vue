<template>
  <section id="about" aria-labelledby="section-title">
    <div class="container">
      <div class="row row-cols-2">
        <div class="col">
          <h5>about the network</h5>
          <h2 id="section-title"><span class="highlight">The</span> Company</h2>
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
            <button>get in touch</button>
            <button>read more</button>
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
  color: #555;
  background-color: $dark-section-bg-clr;
  background-image: url(../assets/img/about-4.jpg);
  background-size: 50%;

  background-position: 100% 50%;
  background-repeat: no-repeat;
}
</style>
