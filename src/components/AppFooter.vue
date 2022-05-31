<template>
  <div>
    <section class="top-section">
      <div class="container">
        <div class="row row-cols-4">
          <div class="col">
            <img src="../assets/img/logo.png" alt="" />
            <p>A functional HTML Template for Corporate & Business.</p>
            <div v-for="(contact, index) in contacts" :key="index">
              <i :class="contact.iconClass"></i>
              {{ contact.info }}
            </div>
            <button class="">get in touch</button>
          </div>
          <div v-for="(item, index) in footerLinks" :key="index" class="col">
            <h4>{{ item.name }}</h4>
            <ul>
              <li v-for="(item, index) in item.contentList" :key="index">
                <i class="fa-solid fa-chevron-right"></i>
                <a href="item.href">{{ item.title }}</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section class="bottom-section">
      <div class="container">
        <div class="row row-cols-2">
          <p>Enjoy the low price. We are tracking any intention of piracy</p>

          <p class="text-end">
            &mark 2020 NEXGEN is Proudly Powered by <span>Codings</span>.
          </p>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "AppFooter",

  props: {
    contacts: Array,
    footerLinks: Array,
    footerLink: Object,
    contentList: Array,
  },
};
</script>

<style lang="scss" scoped></style>
