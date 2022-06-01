<template>
  <section id="projects" aria-labelledby="section-title">
    <div class="container text-center p-0">
      <h5>we do for everyone</h5>
      <h2 id="section-title" class="mt-4">
        Actions & <span class="highlight">Projects</span>
      </h2>
      <nav>
        <ul class="mt-4">
          <li
            v-for="(navItem, index) in navItems"
            :key="index"
            :class="{ highlight: navItem.active }"
            class="py-2"
          >
            <a href="">{{ navItem.name }}</a>
          </li>
        </ul>
      </nav>
      <div class="row row-cols-3 justify-content-between">
        <AppProjectCard
          v-for="(project, index) in projects"
          :key="index"
          :projectCard="project"
        />
      </div>
    </div>
  </section>
</template>

<script>
import AppProjectCard from "./AppProjectCard.vue";
export default {
  name: "AppProjects",
  components: {
    AppProjectCard,
  },

  props: {
    navItems: Array,
    projects: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

h2 span {
  color: $brand-primary-clr;
}

li {
  display: inline-block;
  padding: 0 1rem;
  border-radius: 0.2rem;

  a {
    font-weight: 600;
    color: $medium-text-clr;
    text-transform: uppercase;
  }
}
</style>
