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
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import About from "@/components/About.vue";
import Works from "@/components/Works.vue";

export default {
  components: {
    Header,
    About,
    Works,
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
</style>
