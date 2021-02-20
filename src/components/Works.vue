<template>
  <div class="works container">
    <ComponentTitle text="Works Done" />
    <v-row>
      <v-col class="col-12 px-lg-8 px-md-10">
        <carousel
          :loop="true"
          :navigationEnabled="getWidth < 600 ? false : true"
          navigationNextLabel="<i class='v-icon mdi mdi-chevron-right' style='color: #FFD082; caret-color: #FFD082;'></i>"
          navigationPrevLabel="<i class='v-icon mdi mdi-chevron-left' style='color: #FFD082; caret-color: #FFD082;'></i>"
          :navigationClickTargetSize="1"
          :paginationEnabled="false"
          :perPageCustom="[
            [1264, 3],
            [960, 2],
            [0, 1],
          ]"
          :centerMode="true"
        >
          <slide v-for="(item, index) in work_data" :key="index">
            <v-card
              class="mx-auto works-card text-center"
              color="#393E6A"
              dark
              width="300px"
              :elevation="4"
            >
              <v-img
                height="170"
                src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
                ><v-overlay absolute></v-overlay
              ></v-img>
              <v-card-text>
                <div class="card-title">{{ item.title }}</div>
                <div class="card-subtitle">as {{ item.job }}</div>
              </v-card-text>
            </v-card>
          </slide>
        </carousel>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import ComponentTitle from "@/components/ComponentTitle";
import { Carousel, Slide } from "vue-carousel";

export default {
  name: "About",
  components: {
    ComponentTitle,
    Carousel,
    Slide,
  },
  data() {
    return {
      work_data: [
        {
          title: "Best of Anime",
          job: "Fullstack Developer",
          image: "",
        },
        {
          title: "BaliStay",
          job: "Fullstack Developer",
          image: "",
        },
        {
          title: "Victu",
          job: "Fullstack Developer",
          image: "",
        },
        {
          title: "Kostoo",
          job: "Backend Developer",
          image: "",
        },
      ],
    };
  },
  computed: {
    getWidth() {
      return window.innerWidth;
    },
  },
};
</script>

<style scoped>
.works-card {
  border-radius: 15px;
}

.card-title {
  font-family: "PT Serif", serif;
  font-weight: bold;
  font-size: 18px;
  color: #ffd082;
}

.card-subtitle {
  font-family: "Open Sans", sans-serif;
  font-weight: 300;
  font-size: 14px;
  color: #ffffff;
  margin-top: 5px;
}
</style>

<style>
.works .v-overlay__scrim {
  background-color: #ffd082 !important;
  opacity: 0.15 !important;
}

.works .VueCarousel-wrapper {
  min-height: 255px;
}

.works .VueCarousel-navigation-button {
  border-radius: 100px;
  border: 2px solid #ffd082;
  height: 30px;
  display: flex;
}

.works .VueCarousel-navigation-button:focus {
  outline: 0;
}
</style>