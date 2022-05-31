<template>
  <div id="app">
    <header>
      <AppHeader :navItems="headerNavItems" />
    </header>
    <main>
      <AppServices :services="services" />
      <AppCompany :aboutItems="aboutItems" />
      <AppProjects :navItems="projectsNavItems" :projects="projects" />
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

  data() {
    return {
      // HEADER NAV
      headerNavItems: [
        { name: "home", target: "#home" },
        { name: "services", target: "#services" },
        { name: "about", target: "#about" },
        { name: "projects", target: "#projects" },
        { name: "results", target: "#results" },
        { name: "get in touch", target: "#get-in-touch" },
      ],
      // SERVICES SECTION
      services: [
        {
          iconClass: "fas fa-network-wired",
          title: "Audit & Assurance",
          text: "lorem ipsum dolor bla bla bla",
        },
        {
          iconClass: "fas fa-briefcase",
          title: "Financial Advisory",
          text: "lorem ipsum dolor bla bla bla",
        },
        {
          iconClass: "fas fa-chart-bar",
          title: "Analytics and M&A",
          text: "lorem ipsum dolor bla bla bla",
        },
        {
          iconClass: "fas fa-plane",
          title: "Middle Marketing",
          text: "lorem ipsum dolor bla bla bla",
        },
        {
          iconClass: "fas fa-globe",
          title: "Legal Consulting",
          text: "lorem ipsum dolor bla bla bla",
        },
        {
          iconClass: "fas fa-folder-open",
          title: "Regulatory Risk",
          text: "lorem ipsum dolor bla bla bla",
        },
      ],
      //COMPANY SECTION
      aboutItems: [
        {
          iconClass: "fas fa-medal",
          title: "Tradition",
          text: "Lorem ipsum dolor bla bla bla bla",
        },
        {
          iconClass: "fas fa-lock",
          title: "Security",
          text: "Lorem ipsum dolor bla bla bla bla",
        },
        {
          iconClass: "far fa-edit",
          title: "Certificate",
          text: "Lorem ipsum dolor bla bla bla bla",
        },
        {
          iconClass: "fas fa-graduation-cap",
          title: "Expertise",
          text: "Lorem ipsum dolor bla bla bla bla",
        },
      ],
      //PROJECTS SECTION
      //PROJECTS NAV
      projectsNavItems: [
        {
          name: "all",
          active: true,
        },
        {
          name: "institutional",
          active: false,
        },
        {
          name: "social",
          active: false,
        },
        {
          name: "events",
          active: false,
        },
        {
          name: "innovation",
          active: false,
        },
        {
          name: "environment",
          active: false,
        },
        {
          name: "technology",
          active: false,
        },
      ],
      //PROJECTS CARDS
      projects: [
        {
          imgUrl: "1",
          title: "Academic professional program in social media",
          text: "Lorem ipsum ciao ciao bla bla lorem lorem blavblabla",
        },
        {
          imgUrl: "2",
          title: "President speech at the annual meeting",
          text: "Lorem ipsum ciao ciao bla bla lorem lorem blavblabla",
        },
        {
          imgUrl: "3",
          title: "International business trip to Shanghai",
          text: "Lorem ipsum ciao ciao bla bla lorem lorem blavblabla",
        },
        {
          imgUrl: "4",
          title: "Technology workshop with education theme",
          text: "Lorem ipsum ciao ciao bla bla lorem lorem blavblabla",
        },
        {
          imgUrl: "5",
          title: "Donation of clothes and food to partner NGO",
          text: "Lorem ipsum ciao ciao bla bla lorem lorem blavblabla",
        },
        {
          imgUrl: "6",
          title: "Confraternization of the procurement team",
          text: "Lorem ipsum ciao ciao bla bla lorem lorem blavblabla",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./style/common.scss";
@import "./style/variables.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css";
</style>
