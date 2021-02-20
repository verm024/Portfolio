<template>
  <div class="home">
    <div class="header-container">
      <Header />
    </div>
    <div class="about-container" id="about">
      <About />
    </div>
    <div class="works-container" id="works">
      <Works />
    </div>
    <div class="blog-container" id="blog">
      <Blog />
    </div>
    <div class="contact-container" id="blog">
      <Contact />
    </div>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import About from "@/components/About.vue";
import Works from "@/components/Works.vue";
import Blog from "@/components/Blog.vue";
import Contact from "@/components/Contact.vue";

export default {
  components: {
    Header,
    About,
    Works,
    Blog,
    Contact,
  },
};
</script>

<style scoped>
.header-container {
  background: radial-gradient(
    50% 50% at 50% 50%,
    rgba(33, 36, 61, 0.95) 0%,
    #21243d 100%
  );
}

.about-container {
  background: #21243d;
}

.works-container {
  background: #2b2f4a;
}

.blog-container {
  background: #21243d;
}

.contact-container {
  background: #2b2f4a;
}
</style>
