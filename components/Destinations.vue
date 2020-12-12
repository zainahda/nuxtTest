<template>
  <div>
    <div class="card-group">
      <b-card
        :title="all.name"
        :img-src="all.image"
        :img-alt="all.name"
        img-top
        tag="article"
        style="max-width: 20rem"
        height="150px"
        class="mb-2 "
      >
        <div class="container"></div>
        <div class="bottom-right">
          <b-form-rating
            inline
            :value="all.ratings"
            readonly
            show-value
            precision="1"
            variant="warning"
          ></b-form-rating>
        </div>

        <b-card-text>
          {{ all.address }}
        </b-card-text>
        <div v-b-hover="handleHover" class="border rounded py-3 px-4">
          <b-icon v-if="isHovered" icon="battery-full" scale="100"></b-icon>
          <b-icon v-else icon="battery" scale="2"></b-icon>
          <span class="ml-2" :class="isHovered ? 'text-danger' : ''"
            >Termasuk dalam <br />zona <span>Orange</span> covid-19</span
          >
        </div>
        <div class="overlay">
          <div class="text">
            <p>Patuhilah protokol kesehatan</p>
          </div>
          <b-button class="explore" href="/explore">Explore Now</b-button>
        </div>
      </b-card>
    </div>
  </div>
</template>

<script>
export default {
  data() {
      return {
        isHovered: false
      }
    },
    methods: {
      handleHover(hovered) {
        this.isHovered = hovered
      }
    },
  props: {
    all: {
      type: Object,
      default: () => {},
    },
  },
};
</script>

<style scoped>
.bottom-right {
  position: absolute;
  right: 5px;
  top: 180px;
  border-radius: 10px;
}
.bottom-right p {
  font-size: 20px;
}
.bottom-right svg {
  color: #ffd700;
}

.explore {
  color: white;
  border: 1px solid grey;
  background: linear-gradient(180deg, #fea858 0%, #f85e1d 100%);
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.41));
  margin-left: 10px;
  margin-top: 10px;
}
.explore:hover {
  background: white;
  color: #f85e1d;
}
/* .card-group {
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.41));
}
.home {
  margin-top: -90px;
}
.home:hover {
  color: #f85e1d;
}
.top {
  margin-top: -60px;
  width: 150px;
}
.container {
  position: relative;
  width: 100%;
}
.overlay {
  position: absolute;
  bottom: 100%;
  left: 0;
  right: 0;
  background-color: #008cba;
  overflow: hidden;
  width: 100%;
  height: 0;
  transition: 0.5s ease;
}
.container:hover .overlay {
  bottom: 0;
  height: 100%;
}
.text {
  white-space: nowrap;
  color: white;
  font-size: 17px;
  position: absolute;
  overflow: hidden;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
}
.text span {
  font-weight: bold;
}
.description {
  color: black;
}
.search2 {
  background: linear-gradient(180deg, #fea858 0%, #f85e1d 100%);
} */

/* tablet version */
/* @media (min-width: 768px) {
  .explore {
    margin-left: 170px;
    margin-top: 270px;
  }
  .card-group {
    margin-right: 15px;
  }
} */

/* Desktop Version */
/* @media (min-width: 992px) {
  .container-destination {
    margin-top: 100px;
    margin-left: 250px;
    width: 1440px;
    height: 100%;
    margin-top: -10px;
  }
  .header h1 {
    margin-bottom: 110px;
    justify-content: center;
    font-size: 64px;
    padding: 50px 0 10px 0;
  }
  .card-group {
    justify-content: center;
    margin-right: 10px;
  }
  .home {
    margin-top: -350px;
  }
  .text {
    font-size: 20px;
  }
  .explore {
    margin-left: 90px;
    margin-top: 250px;
  }
} */
</style>