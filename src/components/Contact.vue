<template>
  <div class="contact container">
    <ComponentTitle text="Contact" />
    <div>
      <v-row>
        <v-col class="col-12 col-md-6">
          <v-card color="#393E6A" :elevation="4" class="contact-card">
            <v-card-text class="d-flex justify-space-between align-center">
              <div class="contact-detail">
                <div class="detail-title">Email</div>
                <div class="detail-description">muhnaufal251@gmail.com</div>
              </div>
              <div class="contact-icon">
                <v-icon large color="#FFD082"> mdi-email </v-icon>
              </div>
            </v-card-text>
          </v-card>
        </v-col>
        <v-col class="col-12 col-md-6">
          <v-card color="#393E6A" :elevation="4" class="contact-card">
            <v-card-text class="d-flex justify-space-between align-center">
              <div class="contact-detail">
                <div class="detail-title">LinkedIn</div>
                <div class="detail-description">
                  Muhammad Naufal Arkan Rafii
                </div>
              </div>
              <div class="contact-icon">
                <v-icon large color="#FFD082"> mdi-linkedin </v-icon>
              </div>
            </v-card-text>
          </v-card>
        </v-col>
        <v-col class="col-12 col-md-6">
          <v-card color="#393E6A" :elevation="4" class="contact-card">
            <v-card-text class="d-flex justify-space-between align-center">
              <div class="contact-detail">
                <div class="detail-title">Github</div>
                <div class="detail-description">verm024</div>
              </div>
              <div class="contact-icon">
                <v-icon large color="#FFD082"> mdi-github </v-icon>
              </div>
            </v-card-text>
          </v-card>
        </v-col>
        <v-col class="col-12 col-md-6">
          <v-card color="#393E6A" :elevation="4" class="contact-card">
            <v-card-text class="d-flex justify-space-between align-center">
              <div class="contact-detail">
                <div class="detail-title">Phone</div>
                <div class="detail-description">+6285336181135</div>
              </div>
              <div class="contact-icon">
                <v-icon large color="#FFD082"> mdi-phone </v-icon>
              </div>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </div>
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
    return {};
  },
};
</script>

<style scoped>
.contact-card {
  border-radius: 15px;
  padding: 10px;
}

.detail-title {
  color: #ffd082 !important;
  font-family: "PT Serif", serif;
  font-weight: 700;
  font-size: 18px;
}

.detail-description {
  font-family: "Open Sans", sans-serif;
  font-weight: 300;
  font-size: 14px;
  color: #ffffff;
}
</style>