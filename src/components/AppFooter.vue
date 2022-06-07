<template>
  <div>
    <!-- TOP FOOTER -->
    <section class="top-section">
      <div class="container">
        <div class="row row-cols-4 justify-content-between">
          <div class="col">
            <img src="../assets/img/logo.png" alt="" />
            <p>A Functional HTML Template for Corporate & Business.</p>
            <div v-for="(contact, index) in contacts" :key="index">
              <i :class="contact.iconClass" class="mb-3 me-2"></i>
              {{ contact.info }}
            </div>
            <button class="btn alpha-btn">get in touch</button>
          </div>
          <!-- CARDS -->
          <div
            v-for="(item, index) in footerLinks"
            :key="index"
            class="col links-col p-4"
          >
            <h4 class="mb-3">{{ item.name }}</h4>
            <ul>
              <!-- LINK LISTS -->
              <li
                v-for="(item, index) in item.linksList"
                :key="index"
                class="mt-2"
              >
                <i class="fa-solid fa-chevron-right me-3"></i>
                <a :href="item.href">{{ item.title }}</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>
    <!-- /TOP FOOTER -->
    <!-- BOTTOM FOOTER -->
    <div class="bottom-section py-4">
      <div class="container">
        <div class="row row-cols-2">
          <p>Enjoy the low price. We are tracking any intention of piracy</p>

          <p class="text-end">
            &copy; 2020 NEXGEN is Proudly Powered by <span>Codings</span>.
          </p>
        </div>
      </div>
    </div>
  </div>
  <!-- /BOTTOM-FOOTER -->
</template>

<script>
export default {
  name: "AppFooter",

  props: {
    contacts: Array,
    footerLinks: Array,
    footerLink: Object,
    linksList: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
* {
  color: #fff;
}
.top-section {
  background-color: $dark-section-bg-clr;

  img {
    height: 3rem;
  }

  .links-col {
    width: 22%;
    background-color: #1a1a1f;
    border-radius: 0.5rem;

    h4 {
      text-transform: capitalize;
    }

    ul {
      margin-left: -2rem;

      li {
        text-transform: capitalize;
      }
    }
  }
}

.bottom-section {
  background-color: #111;

  p {
    span {
      color: $brand-primary-clr;
    }
  }
}
</style>
