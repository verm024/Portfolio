<template>
  <v-row class="d-flex align-center justify-center">
    <v-col class="col-lg-2 col-md-3 col-sm-3 d-none d-sm-block text-center">
      <hr />
    </v-col>
    <v-col
      class="col-lg-2 col-md-3 col-sm-4 col-7 text-center pre-component-title"
    >
      {{ text }}
      <hr class="d-sm-none" />
    </v-col>
    <v-col class="col-lg-2 col-md-3 col-sm-3 d-none d-sm-block text-center">
      <hr />
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "ComponentTitle",
  props: ["text"],
  data() {
    return {};
  },
};
</script>

<style scoped>
.pre-component-title {
  font-size: 24px;
  color: #ffd082 !important;
  font-family: "PT Serif", serif;
  font-weight: 700;
}

hr {
  background-color: white;
}
</style>