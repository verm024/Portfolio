<template>
  <v-app>
    <v-app-bar app color="#21243D" dark flat>
      <div class="container d-flex align-center">
        <router-link to="/">
          <div>
            <v-img
              alt="Muhammad Naufal"
              contain
              src="@/assets/logo-naufal.png"
              width="100px"
            />
          </div>
        </router-link>
        <v-btn href="#" text class="ml-auto custom-nav-link">
          <span>Home</span>
        </v-btn>
        <v-btn href="#about" text class="custom-nav-link">
          <span>About</span>
        </v-btn>
        <v-btn href="#works" text class="custom-nav-link">
          <span>Works</span>
        </v-btn>
        <v-btn href="#blog" text class="custom-nav-link">
          <span>Blog</span>
        </v-btn>
        <v-btn
          href="https://wa.me/6285336181135"
          target="_blank"
          text
          class="custom-nav-link custom-nav-contact"
        >
          <span>Contact</span>
        </v-btn>
      </div>
    </v-app-bar>

    <v-main>
      <router-view> </router-view>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data: () => ({}),
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&family=PT+Serif:ital,wght@0,400;0,700;1,400;1,700&display=swap");

html {
  scroll-behavior: smooth;
}

.custom-nav-link {
  font-family: "Open Sans", sans-serif;
  font-weight: 600 !important;
  font-size: 14px !important;
}

.custom-nav-link::before {
  background-color: #21243d !important;
}

.custom-nav-link span {
  transition: 0.1s ease-in-out;
}

.custom-nav-link:hover span {
  color: #ffd082 !important;
}

.custom-nav-contact {
  color: #ffd082 !important;
  border: 2px solid #ffd082;
  margin-left: 15px;
}
</style>
