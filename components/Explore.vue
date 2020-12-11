<template>
  <div>
      <b-nav class="back">
        <b-nav-item href="/" active>Home /</b-nav-item>
        <b-nav-item href="destination">Destination /</b-nav-item>
        <b-nav-item disabled>Explore</b-nav-item>
      </b-nav>
      <div class="container">
      <b-tabs content-class="mt-3" justified text-danger>

        <!-- first tab start-->
        <b-tab title="Details" active>
          <img class="image" src="../assets/bromo.jpg">
          </b-tab>
        <!-- first tab end -->

        <!-- Second tab start -->
        <b-tab title="About">
          <p>{{ text }}</p>
          <p>{{ lokasi }}</p>
        </b-tab>
        <!-- second tab end -->

        <!-- third tab start -->
        <b-tab title="Travel Tips">
          <p class="prokes">Protokol kesehatan<span> di tempat wisata</span></p>
            <b-card-group class="card" deck>
              <b-col cols="3" lg="3" md="4" sm="6">
                <b-card
                  img-src="../assets/healthy.png"
                  img-alt="Image"
                  img-top
                  tag="article"
                  class="icon mb-5"
                >
                  <b-card-text class="description">
                    Pastikan diri dalam kondisi sehat sebelum pergi.
                  </b-card-text>
                </b-card>
              </b-col>

              <b-col cols="3" lg="3" md="4" sm="6">
                <b-card
                  img-src="../assets/stay-at-home.png"
                  img-alt="Image"
                  img-top
                  tag="article"
                  class="icon mb-5"
                >
                <b-card-text class="description">
                    Jika alami gejala sakit, tetap di rumah dan segera berobat
                  </b-card-text>
                </b-card>
              </b-col>

              <b-col cols="3" lg="3" md="4" sm="6">
                <b-card
                  img-src="../assets/patient.png"
                  img-alt="Image"
                  img-top
                  tag="article"
                  class="icon mb-5"
                >
                <b-card-text class="description">
                    Selalu gunakan masker, selama di tempat wisata
                  </b-card-text>
                </b-card>
              </b-col>

              <b-col cols="3" lg="3" md="4" sm="6">
                <b-card
                  img-src="../assets/wash-your-hands.png"
                  img-alt="Image"
                  img-top
                  tag="article"
                  class="icon mb-5"
                >
                <b-card-text class="description">
                    Sering cuci tangan pakai sabun atau handsanitizer
                  </b-card-text>
                </b-card>
              </b-col>

              <b-col cols="3" lg="3" md="4" sm="6">
                <b-card
                  img-src="../assets/keep-distance.png"
                  img-alt="Image"
                  img-top
                  tag="article"
                  class="icon mb-5"
                >
                <b-card-text class="description">
                    Tetap perhatikan jarak, minimal 1 meter
                  </b-card-text>
                </b-card>
              </b-col>

              <b-col cols="3" lg="3" md="4" sm="4">
                <b-card
                  img-src="../assets/shower.png"
                  img-alt="Image"
                  img-top
                  tag="article"
                  class="icon mb-5"
                >
                <b-card-text class="description">
                    Saat tiba di rumah, segera mandi sebelum kontak dengan keluarga
                  </b-card-text>
                </b-card>
              </b-col>

              <b-col cols="3" lg="3" md="4" sm="4">
                <b-card
                  img-src="../assets/cleaning.png"
                  img-alt="Image"
                  img-top
                  tag="article"
                  class="icon mb-5"
                >
                <b-card-text class="description">
                    Bersihkan handphone, kacamata, tas dan barang lainnya dengan disinfektan
                  </b-card-text>
                </b-card>
              </b-col>
        </b-card-group>
          </b-tab>
        <!-- third tab end -->
        
      </b-tabs>
      </div>
  </div>
</template>

<script>
export default {
  data() {
      return {
        text: `
          Gunung Bromo dalam bahasa Tengger dieja "Brama", adalah sebuah gunung berapi aktif di Jawa Timur, Indonesia. Gunung ini memiliki ketinggian 2.329 meter di atas permukaan laut dan berada dalam empat wilayah kabupaten, yakni Kabupaten Probolinggo, Kabupaten Pasuruan, Kabupaten Lumajang, dan Kabupaten Malang. Gunung Bromo terkenal sebagai objek wisata utama di Jawa Timur. Sebagai sebuah objek wisata, Bromo menjadi menarik karena statusnya sebagai gunung berapi yang masih aktif. Gunung Bromo termasuk dalam kawasan Taman Nasional Bromo Tengger Semeru.
        `,
        lokasi:`Letak dan Lokasi Gunung Bromo  secara geografis tepatnya di Provinsi Jawa Timur, tepatnya di kelilingi oleh 4 wilayah pemerintahan Kabupaten karena Gunung Bromo memang terletak di perbatasan Kabupaten tersebut, yaitu Kapupaten Probolinggo, Kabupaten Pasuruan, Kabupaten Malang dan Kabupaten Lumajang.

        Yang unik dari letak dan lokasi Gunung Bromo adalah, terdapat di perbatasan 4 kabupaten di Jawa Timur. Yaitu, kabupaten Malang, kabupaten Pasuruan, kabupaten Probolinggo, dan terakhir adalah kabupaten Lumajang. Namun, jalur terbaik bagi wisatawan yang berasal dari luar kota adalah melalui rute Kabupaten Probolinggo, selain akasesnya mudah dekat dengan Terminal Bayu ANgga Probolinggo dan Stasiun Kereta Api Probolinggo.`,
        info:`
        Termasuk zona orange covid`,
        
        infeksi: `terinfeksi : 62313`,
        sembuh : `sembuh : 54863`,
        meninggal : `meninggal : 4438`,
      }
    }
}
</script>

<style scooped>
.container {
  border: 1px solid black;
  border-radius: 20px;
  height: 850px;
  margin-top: 100px;
  padding: 30px;
}
.info-covid {
  text-align: center;
  background-color: orange;
  font-weight: bold;
}
.image {
  margin-left: 15px;
  margin-bottom: 30px;
  width: 450px;
  height: 400px;
}
.image-info {
  float: left;
  margin-left: 10px;
  width: 250px;
  height: 650px;
}
.info{
  float: right;
  margin-right: 80px;
  font-size: 30px;
}
.list{
  float: right;
  margin-right: 150px;
}
.back{
  color: #F85E1D;
  background-color: white;
  position: absolute;
  width: 500px;
  margin-left: 50px;
  margin-top: -40px;
}
.back:hover {
  background-color: none;
}
.icon {
  width: 50px;
  height: 50px;
  left: 45px;
  border: none;
}
.description {
  display: flex;
  width: 200px;
  margin-left: -50px;
  font-size: 15px;
  width: 200px;

}
.card{
  margin-top: 60px;
  border: none;
}
.prokes{
  color: #000080;
  text-transform: uppercase;
  position: relative;
  font-size: 18px;
  margin: 20px 0 -60px 50px;
}
span{
  font-weight: bold;
}
/* tablet version */
@media (min-width: 768px) {
  .image {
  width: 90%;
  height: 90%;
}
.image-info {
  width: 60%px;
  height: 10%px;
}
.back{
  margin-left: 425px;
  margin-top: -40px;
}
.icon {
  width: 50px;
  height: 50px;
  left: 45px;
  border: none;
}
}

/* Desktop Version */
@media (min-width: 992px) {
.container {
  height: 782px;
}
.icon {
  width: 150px;
  height: 150px;
}
.prokes{
  font-size: 40px;
  margin: 20px 0 -50px 110px;
}
.back{
  margin-left: 400px;
}
.image-info {
  width: 500px;
  height: 650px;
}
}
</style>