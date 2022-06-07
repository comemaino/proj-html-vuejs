<template>
  <div id="app">
    <header>
      <AppHeader
        :navItems="headerNavItems"
        :contacts="contacts"
        :socialMedia="socialMedia"
      />
    </header>
    <main>
      <AppServices :services="services" />
      <AppCompany :aboutItems="aboutItems" />
      <AppProjects :navItems="projectsNavItems" :projects="projects" />
      <AppResults :results="results" :logos="logos" />
      <AppCta :contacts="contacts" />
    </main>
    <footer>
      <AppFooter
        :contacts="contacts"
        :footerLinks="footerLinks"
        :linksList="footerLinks.linksList"
      />
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
      // CONTACTS
      contacts: [
        {
          iconClass: "fas fa-phone-alt",
          info: "+1 (305) 1234-5678",
        },
        {
          iconClass: "fas fa-envelope",
          info: "hello@example.com",
        },
        {
          iconClass: "fas fa-map-marker-alt",
          info: "Main Avenue, 987",
        },
      ],
      // SOCIAL MEDIA
      socialMedia: [
        {
          link: "https://www.facebook.com",
          iconClass: "fab fa-facebook-f",
        },
        {
          link: "https://www.twitter.com",
          iconClass: "fab fa-twitter",
        },
        {
          link: "https://www.linkedin.com",
          iconClass: "fab fa-linkedin-in",
        },
      ],
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
          text: "lorem ipsum dolor bla bla bla lorem ipsum dolor bla bla bla",
        },
        {
          iconClass: "fas fa-briefcase",
          title: "Financial Advisory",
          text: "lorem ipsum dolor bla bla bla lorem ipsum dolor bla bla bla",
        },
        {
          iconClass: "fas fa-chart-bar",
          title: "Analytics and M&A",
          text: "lorem ipsum dolor bla bla bla lorem ipsum dolor bla bla bla",
        },
        {
          iconClass: "fas fa-plane",
          title: "Middle Marketing",
          text: "lorem ipsum dolor bla bla bla lorem ipsum dolor bla bla bla",
        },
        {
          iconClass: "fas fa-globe",
          title: "Legal Consulting",
          text: "lorem ipsum dolor bla bla bla lorem ipsum dolor bla bla bla",
        },
        {
          iconClass: "fas fa-folder-open",
          title: "Regulatory Risk",
          text: "lorem ipsum dolor bla bla bla lorem ipsum dolor bla bla bla",
        },
      ],
      // COMPANY SECTION
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
      // PROJECTS SECTION
      // PROJECTS NAV
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
      // PROJECTS CARDS
      projects: [
        {
          imgUrlId: "1",
          title: "Academic professional program in social media",
          text: "Lorem ipsum ciao ciao bla bla lorem lorem blavblabla",
        },
        {
          imgUrlId: "2",
          title: "President speech at the annual meeting",
          text: "Lorem ipsum ciao ciao bla bla lorem lorem blavblabla",
        },
        {
          imgUrlId: "3",
          title: "International business trip to Shanghai",
          text: "Lorem ipsum ciao ciao bla bla lorem lorem blavblabla",
        },
        {
          imgUrlId: "4",
          title: "Technology workshop with education theme",
          text: "Lorem ipsum ciao ciao bla bla lorem lorem blavblabla",
        },
        {
          imgUrlId: "5",
          title: "Donation of clothes and food to partner NGO",
          text: "Lorem ipsum ciao ciao bla bla lorem lorem blavblabla",
        },
        {
          imgUrlId: "6",
          title: "Confraternization of the procurement team",
          text: "Lorem ipsum ciao ciao bla bla lorem lorem blavblabla",
        },
      ],

      results: [
        // COMPANY NUMBERS
        {
          category: "certifications",
          amount: 128,
        },
        {
          category: "employees",
          amount: 230,
        },
        {
          category: "costumers",
          amount: 517,
        },
        {
          category: "countries served",
          amount: 94,
        },
      ],

      // TECHNOLOGIES
      logos: [
        {
          imgUrlId: "4",
          imgAlt: "jquery-logo",
        },
        {
          imgUrlId: "5",
          imgAlt: "less-logo",
        },
        {
          imgUrlId: "1",
          imgAlt: "woo-commerce-logo",
        },
        {
          imgUrlId: "2",
          imgAlt: "wordpress-logo",
        },
        {
          imgUrlId: "3",
          imgAlt: "pingdom-logo",
        },
      ],

      // FOOTER
      // FOOTER ABOUT
      footerLinks: [
        {
          name: "about",
          linksList: [
            {
              title: "the company",
              href: "",
            },
            {
              title: "institutional",
              href: "",
            },
            {
              title: "social & events",
              href: "",
            },
            {
              title: "innovation",
              href: "",
            },
            {
              title: "environment",
              href: "",
            },
            {
              title: "technology",
              href: "",
            },
          ],
        },
        // FOOTER SERVICES
        {
          name: "services",
          linksList: [
            {
              title: "audit & assurance",
              href: "",
            },
            {
              title: "financial advisory",
              href: "",
            },
            {
              title: "analytics M&A",
              href: "",
            },
            {
              title: "middle marketing",
              href: "",
            },
            {
              title: "legal consulting",
              href: "",
            },
            {
              title: "regulatory risk",
              href: "",
            },
          ],
        },
        // FOOTER SUPPORT
        {
          name: "support",
          linksList: [
            {
              title: "responsability",
              href: "",
            },
            {
              title: "terms of use",
              href: "",
            },
            {
              title: "about cookies",
              href: "",
            },
            {
              title: "privacy policy",
              href: "",
            },
            {
              title: "accessibility",
              href: "",
            },
            {
              title: "information",
              href: "",
            },
          ],
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
