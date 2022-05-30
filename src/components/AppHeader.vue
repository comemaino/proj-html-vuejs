<template>
  <div>
    <!-- HEADER -->
    <div class="top-bar">
      <div class="container">
        <div class="row">
          <div class="col-4">
            <i class="fas fa-clock"></i>
            Open Hours: Mon - Sat - 9:00 - 18:00
          </div>
          <div class="col-8 justify-content-end text-end">
            <div class="row row-cols-3">
              <div class="col">
                <i class="fas fa-phone-alt"></i>
                +1 (305) 1234-5678
              </div>
              <div class="col">
                <i class="fas fa-envelope"></i>
                hello@example.com
              </div>
              <div class="col incons">
                <i class="fab fa-facebook-f p-2"></i>
                <i class="fab fa-twitter p-2"></i>
                <i class="fab fa-linkedin-in p-2"></i>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- /HEADER -->
    <!-- JUMBOTRON -->
    <div class="jumbotron">
      <div class="container h-100">
        <nav>
          <div class="row">
            <div class="col-4">
              <img src="../assets/img/logo.png" alt="" class="logo" />
            </div>
            <div class="col-8 text-end">
              <ul class="nav-links">
                <li
                  v-for="(navItem, index) in navItems"
                  :key="index"
                  :navItem="navItem"
                >
                  <a :href="navItem.target">{{ navItem.name }}</a>
                </li>
              </ul>
            </div>
          </div>
        </nav>
        <div class="row h-100 justify-content-center align-items-center">
          <div class="jumbo-content w-50 text-center">
            <h1>ready <span class="highlight">team</span></h1>
            <p>
              No matter what your company needs, we will be ready to assist you
              in the best possible way.
            </p>
            <button>get in touch</button>
            <button>read more</button>
          </div>
        </div>
      </div>
    </div>
    <!-- /JUMBOTRON -->
  </div>
</template>

<script>
export default {
  name: "AppHeader",

  props: {
    navItems: Array,
  },
};
</script>

<style lang="scss" scoped>
.jumbotron {
  padding: 1rem;
  height: 50rem;
  background-image: url(../assets/img/bg-parallax.png);
  background-size: auto;
  background-position: center;

  .logo {
    width: 10rem;
  }

  li {
    display: inline-block;
    padding: 0 1rem;
  }
}
</style>
