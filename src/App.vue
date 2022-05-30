<template>
  <div id="app">
    <header>
      <AppHeader />
    </header>
    <main>
      <AppServices />
      <AppCompany />
      <AppProjects />
      <AppResults />
      <AppCta />
    </main>
    <footer>
      <AppFooter />
    </footer>
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppServices from "./components/AppServices.vue";
import AppCompany from "./components/AppCompany.vue";
import AppProjects from "./components/AppProjects.vue";
import AppResults from "./components/AppResults.vue";
import AppCta from "./components/AppCta.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppServices,
    AppCompany,
    AppProjects,
    AppResults,
    AppCta,
    AppFooter,
  },
};
</script>

<style lang="scss">
@import "./style/common.scss";
@import "./style/variables.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css";
</style>
