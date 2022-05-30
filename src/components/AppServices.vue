<template>
  <section id="services" aria-labelledby="section-title">
    <div class="container">
      <div class="row justify-content-between align-items-end">
        <div class="col-9">
          <h5>our business area</h5>
          <h2 id="section-title">
            Excellence in <span class="highlight">Services</span>
          </h2>

          <p>
            We are leaders in providing consultancy services with a set of
            cutting-efge technologies and a team of experienced and renowned
            professionals. These are some options that you can hire.
          </p>
        </div>
        <div class="col-3 text-end">
          <button>see all</button>
        </div>
      </div>
      <div class="row row-cols-3">
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
  background-color: $clear-section-bg-clr;
}
</style>
