<template>
  <section id="projects" aria-labelledby="section-title">
    <div class="container text-center">
      <h5>we do for everyone</h5>
      <h2 id="section-title">
        Actions & <span class="highlight">Projects</span>
      </h2>
      <nav>
        <ul>
          <li
            v-for="(navItem, index) in navItems"
            :key="index"
            :navItem="navItem"
            :class="{ highlight: navItem.active }"
          >
            <a href="">{{ navItem.name }}</a>
          </li>
        </ul>
      </nav>
      <div class="row row-cols-3">
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
li {
  display: inline-block;
  padding: 0 1rem;
}
</style>
