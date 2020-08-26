<template>
    <v-app>
        <v-app-bar
          app
          color="#21243D"
          dark
          flat
        >
            <div class="container d-flex align-center">
                <div>
                    <v-img alt="Muhammad Naufal" contain src="@/assets/logo-naufal.png" width="100px"/>
                </div> 
                <v-btn href="#" text class="ml-auto custom-nav-link">
                    <span>Home</span>
                </v-btn>
                <v-btn href="#about" text class="custom-nav-link">
                    <span>About</span>
                </v-btn>
                <v-btn href="https://github.com/vuetifyjs/vuetify/releases/latest" target="_blank" text class="custom-nav-link">
                    <span>Works</span>
                </v-btn>
                <v-btn href="https://github.com/vuetifyjs/vuetify/releases/latest" target="_blank" text class="custom-nav-link">
                    <span>Blog</span>
                </v-btn>
                <v-btn href="https://github.com/vuetifyjs/vuetify/releases/latest" target="_blank" text class="custom-nav-link">
                    <span>Contact</span>
                </v-btn>
            </div>
        </v-app-bar>

        <v-main>
            <router-view>
              
            </router-view>
        </v-main>
    </v-app>
</template>

<script>

export default {
    data: () => ({
      
    }),
};
</script>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&family=PT+Serif:ital,wght@0,400;0,700;1,400;1,700&display=swap');

    .custom-nav-link{
        font-family: 'Open Sans', sans-serif;
        font-weight: 500 !important;
        font-size: 14px !important;
    }

    .custom-nav-link::before{
      background-color: #21243D !important;
    }

    .custom-nav-link span{
      transition: .1s ease-in-out;
    }

    .custom-nav-link:hover span{
        color: #FFD082 !important;
    }
</style>
