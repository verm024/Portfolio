<template>
  <v-row class="d-flex align-center">
    <v-col class="col-5 text-center">
      <hr />
    </v-col>
    <v-col class="col-2 text-center pre-component-title"> {{ text }} </v-col>
    <v-col class="col-5 text-center">
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