<template>
  <div class="container">
    <h1 class="header">Populars Destination</h1>
    <div class="carousel-wrapper">
      <VueSlickCarousel v-bind="settings">
        <div
          v-for="popular in populars.results.slice(0, 10)"
          :key="popular.id"
          :popular="popular"
          class="img-wrapper"
        >
          <img :src="popular.image" />
        </div>
      </VueSlickCarousel>
    </div>
  </div>
</template>

<script>
export default {
  async fetch() {
    this.populars = await fetch(
      "https://travvago-backend.herokuapp.com/api/v1/destination/populars?page=1"
    ).then((res) => res.json());
  },
  data() {
    return {
      populars: [],
      settings: {
        arrows: false,
        dots: false,
        focusOnSelect: true,
        infinite: true,
        speed: 500,
        slidesToShow: 3,
        slidesToScroll: 3,
        touchThreshold: 5,
      },
    };
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Satisfy&display=swap");

.header {
  display: flex;
  font-family: "Satisfy", cursive;
  margin-bottom: 10px;
  color: #f85e1d;
  justify-content: center;
  font-weight: bold;
  font-size: 48px;
  padding: 40px 0 10px 0;
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.41));
}
.carousel-wrapper {
  padding: 40px;
}
.img-wrapper img {
  margin: auto;
  width: 300px;
  height: 250px;
  background-image: linear-gradient(gray 100%, transparent 0);
}
</style>