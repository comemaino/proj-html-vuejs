<template>
  <section id="services" aria-labelledby="services-section-title">
    <div class="container">
      <div class="row justify-content-between align-items-end">
        <div class="col-9 p-0">
          <h5>our business area</h5>
          <h2 id="services-section-title">
            Excellence in <span class="highlight">Services</span>
          </h2>

          <p>
            We are leaders in providing consultancy services with a set of
            cutting-efge technologies and a team of experienced and renowned
            professionals. These are some options that you can hire.
          </p>
        </div>
        <div class="col-3 text-end p-0">
          <button class="btn brand-btn mb-4">see all</button>
        </div>
      </div>
      <div class="row justify-content-between">
        <AppServiceCard
          v-for="(serviceItem, index) in services"
          :key="index"
          :serviceCard="serviceItem"
        />
      </div>
    </div>
  </section>
</template>

<script>
import AppServiceCard from "./AppServiceCard.vue";

export default {
  name: "AppServices",

  props: {
    services: Array,
  },

  components: {
    AppServiceCard,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
#services {
  background-color: $light-section-bg-clr;

  h2 {
    span {
      color: $brand-primary-clr;
    }
  }
}
</style>
