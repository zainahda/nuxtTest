<template>
  <div>
    <h1 class="header">Galery</h1>
    <div class="carousel-wrapper">
      <VueSlickCarousel v-bind="settings">
        <div
          v-for="all in all.results"
          :key="all.id"
          :all="all"
          class="img-wrapper"
        >
          <img :src="all.image" />
        </div>
      </VueSlickCarousel>
    </div>
  </div>
</template>

<script>
export default {
  async fetch() {
    this.all = await fetch(
      "https://travvago-backend.herokuapp.com/api/v1/destination/all?page=1"
    ).then((res) => res.json());
  },
  data() {
    return {
      all: [],
      settings: {
        arrows: false,
        infinite: true,
        slidesToShow: 3,
        slidesToScroll: 1,
        autoplay: true,
        autoplaySpeed: 2000,
        pauseOnDotsHover: true,
        pauseOnFocus: true,
        pauseOnHover: true,
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
  width: 600px;
  height: 400px;
  background-image: linear-gradient(gray 100%, transparent 0);
}
</style>