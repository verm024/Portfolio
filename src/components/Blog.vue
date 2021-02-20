<template>
  <div class="blog container">
    <ComponentTitle text="My Blog" />
    <v-row>
      <v-col class="col-12 px-lg-8 px-md-10">
        <div v-for="(item, index) in blog" :key="index">
          <v-card class="d-flex blog-card" color="#393E6A" :elevation="4">
            <v-img
              height="200px"
              max-width="300px"
              src="https://cdn.pixabay.com/photo/2020/07/12/07/47/bee-5396362_1280.jpg"
            />
            <div class="blog-item">
              <div class="blog-title">
                {{ item.title }}
              </div>
              <div class="blog-description">
                {{ item.description }}
              </div>
              <div class="blog-button">
                <v-btn :href="item.link" target="_blank" text>
                  Read More
                </v-btn>
              </div>
            </div>
          </v-card>
        </div>
        <div class="load-more">
          <v-btn class="load-button" color="#ffd082"> load more </v-btn>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import ComponentTitle from "@/components/ComponentTitle";

export default {
  name: "Blog",
  components: {
    ComponentTitle,
  },
  data() {
    return {
      blog: [
        {
          title: "Blog 1",
          description: "This is description 1",
          link:
            "https://www.coursera.org/learn/computer-networking/home/welcome",
        },
        {
          title: "Blog 2",
          description: "This is description 2",
          link: "",
        },
      ],
    };
  },
};
</script>

<style scoped>
.blog-card {
  border-radius: 15px;
}

.blog-item {
  padding: 30px;
}

.blog-title {
  color: #ffd082 !important;
  font-family: "PT Serif", serif;
  font-weight: 700;
  font-size: 18px;
}

.blog-description {
  font-family: "Open Sans", sans-serif;
  font-weight: 300;
  font-size: 14px;
  color: #ffffff;
}

.blog-button .v-btn {
  font-family: "Open Sans", sans-serif;
  font-weight: 600 !important;
  font-size: 12px !important;
  color: #ffd082 !important;
  border: 2px solid #ffd082;
}

.blog-button .v-btn::before {
  background-color: #21243d !important;
}

.blog-button .v-btn span {
  transition: 0.1s ease-in-out;
}

.load-more {
  text-align: center;
}

.load-button {
  color: #21243d;
  font-family: "PT Serif", serif;
  font-weight: 700;
  font-size: 16px;
  letter-spacing: 0px;
  padding-left: 24px !important;
  padding-right: 24px !important;
}
</style>