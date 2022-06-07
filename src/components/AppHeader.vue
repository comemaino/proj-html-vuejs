<template>
  <div>
    <!-- HEADER -->
    <div class="top-bar">
      <div class="container">
        <div class="row justify-content-between">
          <div class="col-4">
            <i class="fas fa-clock"></i>
            Open Hours: Mon - Sat - 9:00 - 18:00
          </div>
          <div class="col-7">
            <div class="row row-cols-3 justify-content-between text-end">
              <div
                v-for="(contact, index) in contacts.slice(0, 2)"
                :key="index"
              >
                <a href=""
                  ><i :class="contact.iconClass" class="me-2"></i
                  >{{ contact.info }}</a
                >
              </div>
              <div class="icons">
                <a
                  v-for="(item, index) in socialMedia"
                  :key="index"
                  :href="item.link"
                  ><i :class="item.iconClass" class="px-3"></i
                ></a>
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
        <!-- NAV -->
        <nav>
          <div class="row">
            <div class="col-4">
              <img src="../assets/img/logo.png" alt="" class="logo" />
            </div>
            <div class="col-8 text-end">
              <ul class="nav-links">
                <li v-for="(navItem, index) in navItems" :key="index">
                  <a
                    :href="navItem.target"
                    :class="{ 'btn brand-btn': index === navItems.length - 1 }"
                    >{{ navItem.name }}
                  </a>
                </li>
              </ul>
            </div>
          </div>
        </nav>
        <!-- /NAV -->
        <div class="row h-100 justify-content-center align-items-center">
          <div
            class="jumbo-content w-50 text-center d-flex flex-column align-items-center"
          >
            <h1>ready <span class="highlight">team</span></h1>
            <p class="my-4">
              No matter what your company needs, we will be ready to assist you
              in the best possible way.
            </p>
            <div class="btn-wrapper">
              <button class="btn brand-btn">
                <a href="#get-in-touch">get in touch</a>
              </button>
              <button class="btn light-btn ms-4">read more</button>
            </div>
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
    contacts: Array,
    navItems: Array,
    socialMedia: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

a:hover {
  color: $brand-primary-clr;
}

.top-bar {
  padding: 1rem 0;
  color: $light-section-bg-clr;
  background-color: $header-bg-clr;
}

.jumbotron {
  padding: 1rem;
  height: 50rem;
  background-image: url(../assets/img/bg-parallax.png),
    url(../assets/img/jumbo-bg.png);

  background-size: auto;
  background-position: center;

  .logo {
    width: 8rem;
  }

  li {
    display: inline-block;

    a {
      padding: 0.5rem 1.25rem;
      font-weight: 500;
      text-transform: uppercase;
    }
  }
  h1 {
    font-size: 4rem;
    font-weight: 900;
    text-transform: capitalize;

    span {
      color: $brand-primary-clr;
    }
  }

  p {
    width: 65%;
  }
}
</style>
