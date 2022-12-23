<template>
  <b-row class="layoute-container" id="layouteContainer" style="background-color: #051622;">
    <b-col lg="2" md="3" sm="12">
      <sidebar class="layoute-navbar-fix"></sidebar>
    </b-col>
    <b-col lg="10" md="9" sm="12">
      <Header class="layoute-navbar-fix" id="layouteHeader" style="background-color: #051622;"></Header>
      <Nuxt />
    </b-col>
  </b-row>
</template>

<script>
export default {
  name: "layoutes",
  data() {
    return {

    }
  },
  methods: {

  }
};
</script>

<style>
.layoute-container {
  padding: 0 10vw;
}

.layoute-navbar-fix {
  position: sticky;
  top: 0;
  z-index: 1;
}

.row {
  margin: 0;
}

@media only screen and (max-width: 1600px) {
  .layoute-container {
    padding: 0 2vw;
  }
}

@media only screen and (max-width: 727px) {
  .layoute-container {
    padding: 0 2vw;
  }
}
</style>
  