<template>
  <section id="get-in-touch" aria-labelledby="section-title">
    <div class="container">
      <div class="row">
        <div class="col-8">
          <h5>send a message</h5>
          <h2 id="section-title">Get in<span class="highlight">Touch</span></h2>
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
          <button>send</button>
        </div>
        <div class="col-4">
          <div class="text-wrapper">
            <h3>Example Inc</h3>
            <p>
              Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ducimus
              quod ex iste soluta at autem nihil. <br />
              Odit fugiat est iusto eaque, consequatur eum inventore veritatis
              assumenda quae nisi, nesciunt sunt!
            </p>
          </div>
          <div class="col" v-for="(contact, index) in contacts" :key="index">
            <i :class="contact.iconClass"></i>
            {{ contact.info }}
          </div>
          <button class="">view map</button>
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
.form-group {
  position: relative;
  margin-top: 1rem;

  &.case-sensitive::after {
    content: "\f151";
    font-family: FontAwesome;
    position: absolute;
    right: 1.5rem;
    bottom: 25%;
    z-index: 10;
  }
}
</style>
