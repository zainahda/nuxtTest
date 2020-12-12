<template>
  <div>
    <Navbar />
    <Landing />
    <!-- populars star -->
    <Populars/>
    <!-- populars end -->
    <!-- destination card start -->
    <div class="container">
      <div class="header">
        <h1 class="animate__animated animate__bounce">Destination</h1>
      
      <div class="row mb-4">
        <div
          class="col-md3 mt-4 ml-3 mr-4"
          v-for="all in all.results.slice(0, 12)"
          :key="all.id"
          
        >
          <Destinations :all="all" />
        </div>
      </div>
    </div>
    </div>
    <Galery/>
    <!-- destination card end -->
    <!-- <ProductCard
  v-for="popular in populars.results"
  :key="popular.id"
  :popular="popular"/> -->
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
    };
  },
  // async fetch(){
  //   this.populars = await fetch(
  //     'https://travvago-backend.herokuapp.com/api/v1/destination/populars?page=2'
  //   ).then((res) => res.json())
  // },
  // data() {
  //   return {
  //     populars: []
  //   }
  // }
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Satisfy&display=swap");
.header h1 {
  display: flex;
  font-family: "Satisfy", cursive;
  margin-bottom: 50px;
  color: #f85e1d;
  justify-content: center;
  font-weight: bold;
  font-size: 48px;
  padding: 40px 0 10px 0;
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.41));
}
</style>
