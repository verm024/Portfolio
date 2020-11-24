<template>
  <div class="about container">
    <ComponentTitle text="About Me" />
    <v-row>
      <v-col class="col-8 offset-2 text-center">
        <span class="about-text">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco
        </span>
      </v-col>
    </v-row>
    <template>
      <v-tabs
        color="21243D"
        v-model="about_tab"
        class="about-tab"
        background-color="#21243D"
      >
        <v-tab @click="setRadius(0)">
          <span class="about-tab-title"> MAIN FOCUS </span>
        </v-tab>
        <v-tab @click="setRadius(1)">
          <span class="about-tab-title"> TESTIMONIALS </span>
        </v-tab>
      </v-tabs>
      <v-tabs-items
        v-model="about_tab"
        class="about-tab-items"
        :style="'border-top-left-radius: ' + tab_items_radius + 'px'"
      >
        <v-tab-item>
          <div
            style="overflow: auto"
            class="text-center about-tab-item-1 d-flex about-tab-item"
          >
            <div>
              <v-card
                class="about-tab-card-1 about-tab-card"
                width="200px"
                color="#393E6A"
                :elevation="4"
              >
                <v-card-text>
                  <div class="about-tab-card-icon">
                    <v-icon color="#21243D" size="30px">mdi-application</v-icon>
                  </div>
                  <span class="about-tab-card-text"> Fullstack </span>
                </v-card-text>
              </v-card>
            </div>
            <div>
              <v-card
                class="about-tab-card-2 about-tab-card"
                width="200px"
                color="#393E6A"
                :elevation="4"
              >
                <v-card-text>
                  <div class="about-tab-card-icon">
                    <v-icon color="#21243D" size="30px">mdi-cog</v-icon>
                  </div>
                  <span class="about-tab-card-text"> Backend </span>
                </v-card-text>
              </v-card>
            </div>
            <div>
              <v-card
                class="about-tab-card-3 about-tab-card"
                width="200px"
                color="#393E6A"
                :elevation="4"
              >
                <v-card-text>
                  <div class="about-tab-card-icon">
                    <v-icon color="#21243D" size="30px">mdi-brush</v-icon>
                  </div>
                  <span class="about-tab-card-text"> Frontend </span>
                </v-card-text>
              </v-card>
            </div>
          </div>
        </v-tab-item>
        <v-tab-item>
          <div class="about-tab-item-2 about-tab-item">Testtttt2</div>
        </v-tab-item>
      </v-tabs-items>
    </template>
  </div>
</template>

<script>
import ComponentTitle from "@/components/ComponentTitle";

export default {
  name: "About",
  components: {
    ComponentTitle,
  },
  data() {
    return {
      about_tab: null,
      tab_items_radius: 0,
    };
  },
  methods: {
    setRadius(id) {
      if (id == 1) {
        this.tab_items_radius = 15;
      } else {
        this.tab_items_radius = 0;
      }
    },
  },
};
</script>

<style scoped>
.about-text {
  color: white;
  font-family: "Open Sans", sans-serif;
  font-weight: 400;
  font-size: 16px;
}

.about-tab .v-tab--active {
  background-color: #ffd082;
  border: none;
}

.about-tab .v-tab {
  border-top-right-radius: 15px;
  border-top-left-radius: 15px;
  padding-left: 50px;
  padding-right: 50px;
}

.about-tab-title {
  color: #ffd082;
  font-family: "PT Serif", serif;
  font-weight: 700;
  font-size: 16px;
  letter-spacing: 0px;
}

.about-tab .v-tab--active .about-tab-title {
  color: #21243d;
}

.about-tab-items {
  background-color: #21243d !important;
  border: 2px solid #ffd082;
  border-radius: 15px;
}

.about-tab-item-1 {
  margin-top: 60px;
  margin-bottom: 60px;
}

.about-tab-card-1 {
  margin-right: 100px;
}

.about-tab-card-3 {
  margin-left: 100px;
}

.about-tab-card {
  padding-top: 30px;
  padding-bottom: 30px;
  border-radius: 15px !important;
}

.about-tab-card-icon {
  width: 60px;
  height: 60px;
  margin-left: auto;
  margin-right: auto;
  background-color: #ffd082;
  vertical-align: middle;
  border-radius: 100px;
  margin-bottom: 20px;
}

.about-tab-card-icon i {
  line-height: 60px !important;
}

.about-tab-card-text {
  color: white;
  font-family: "Open Sans", sans-serif;
  font-weight: 400;
  font-size: 14px;
}
</style>

<style>
.about-tab .v-tabs-slider {
  background-color: #ffd082 !important;
}

@media only screen and (min-width: 960px) {
  .about-tab-item-1 {
    justify-content: space-evenly;
  }
}
</style>