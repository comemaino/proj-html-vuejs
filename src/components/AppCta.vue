<template>
  <section id="get-in-touch" aria-labelledby="section-title">
    <div class="container p-0">
      <div class="row">
        <div class="col-8">
          <h5>send a message</h5>
          <h2 id="section-title" class="my-3">
            Get in <span class="highlight">Touch</span>
          </h2>
          <p>We will respond as soon as possible.</p>

          <form>
            <div class="row row-cols-2">
              <div class="form-group case-sensitive">
                <input
                  type="name"
                  class="form-control"
                  id="name"
                  placeholder="Name"
                />
              </div>
              <div class="form-group case-sensitive">
                <input
                  type="email"
                  class="form-control"
                  id="email"
                  placeholder="Email"
                />
              </div>
              <div class="form-group">
                <input
                  type="phone"
                  class="form-control"
                  id="phone"
                  placeholder="Phone"
                />
              </div>
              <div class="form-group">
                <input
                  type="info"
                  class="form-control"
                  id="info"
                  placeholder="More Info"
                />
              </div>

              <div class="flex-grow-1 form-group">
                <textarea
                  class="form-control"
                  id="message"
                  rows="5"
                  placeholder="Message"
                ></textarea>
              </div>
            </div>
          </form>
          <button class="btn brand-btn mt-4">send</button>
        </div>
        <div class="col-4">
          <div class="text-wrapper">
            <h4>Example Inc.</h4>
            <p>
              Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ducimu
            </p>
            <p>
              Odit fugiat est iusto eaque, consequatur eum inventore veritatis
            </p>
          </div>
          <div
            class="contact mt-3"
            v-for="(contact, index) in contacts"
            :key="index"
          >
            <i class="text-center" :class="contact.iconClass"></i>
            {{ contact.info }}
          </div>
          <button class="btn light-btn mt-3">view map</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppCta",

  props: {
    contacts: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

h2 span {
  color: $brand-primary-clr;
}

.form-group {
  position: relative;
  margin-top: 1rem;

  .form-control {
    border: 0;
    background-color: $light-section-bg-clr;
  }

  &.case-sensitive::after {
    content: url(../assets/img/capslock.png);
    position: absolute;
    right: 1.2rem;
    bottom: 15%;
    z-index: 10;
  }
}

h4 {
  font-weight: 700;
}

p {
  color: $medium-text-clr;
}

.contact {
  color: $brand-primary-clr;

  i {
    width: 2.2rem;
    height: 2.2rem;
    line-height: 2.2rem;
    vertical-align: middle;
    border-radius: 50%;

    background-color: $brand-secondary-clr;
  }
}
</style>
