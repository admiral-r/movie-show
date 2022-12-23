<template>
  <div id="homePage" style="color: white;">
    <img class="w-100 homePage-border-radius" src="../static/images/Lightyear-bg.png">
    <div class="d-flex justify-content-between align-items-center mt-5 mb-4 mx-3">
      <h3 class="mb-0 pointer">Movies</h3>
      <h6 class="mb-0 pointer">see all</h6>
    </div>
    <b-row>
      <b-col md="2" sm="3" v-for="(item, index) in movies" :key="index">
        <div class="mb-5 pointer">
          <a href="" class="homePage-banner d-flex">
            <img :src="`/_nuxt/static/images/${item.name}.png`" class="w-100 homePage-border-radius">
            <div class="homePage-banner-name d-flex justify-content-center align-items-end w-100 h-100 homePage-border-radius">
              <div class="text-center pb-2">
                <h6 class="font-weight-bold mb-1">{{ item.name }}</h6>
                <h6>{{ item.category }}</h6>
              </div>
            </div>
          </a>
        </div>
      </b-col>

    </b-row>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  data() {
    return {
      movies: [
        { id: 0, category: 'Action', name: 'Carter' },
        { id: 1, category: 'Fantasy', name: 'Good and Evil' },
        { id: 2, category: 'Comedy', name: 'Me Time' },
        { id: 3, category: 'Drama', name: 'Adam Project' },
        { id: 4, category: 'Fantasy', name: 'Oxygen' },
        { id: 6, category: 'Fantasy', name: '365 Days' },
      ],
    }
  },
};
</script>

<style>
.homePage-border-radius {
  border-radius: 1rem;
}

.homePage-banner {
  width: 100%;
  transition: filter .5s;
  position: relative;
  overflow: hidden;
}

.homePage-banner:hover {
  filter: contrast(120%);
}

.homePage-banner:hover .homePage-banner-name {
  opacity: 0;
}


.homePage-banner-name {
  background: linear-gradient(180deg, hsla(0, 0%, 96.1%, 0) 40%, #000000);
  color: #ffffff !important;
  position: absolute;
  bottom: 0;
  right: 0;
  left: 0;
  transition: all .3s ease-in-out;
  opacity: 1;
}
</style>