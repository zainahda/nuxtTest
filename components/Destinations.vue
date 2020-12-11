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
        height="200px"
        class="mb-2"
      >
        <div class="container"></div>
        <div class="bottom-right">
          <p>
            Rating
            <svg
              width="12px"
              height="12px"
              viewBox="0 0 16 16"
              class="bi bi-star-fill"
              fill="currentColor"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M3.612 15.443c-.386.198-.824-.149-.746-.592l.83-4.73L.173 6.765c-.329-.314-.158-.888.283-.95l4.898-.696L7.538.792c.197-.39.73-.39.927 0l2.184 4.327 4.898.696c.441.062.612.636.283.95l-3.523 3.356.83 4.73c.078.443-.36.79-.746.592L8 13.187l-4.389 2.256z"
              />
            </svg>
            {{ all.ratings }}
          </p>
        </div>

        <b-card-text>
          {{ all.address }}
        </b-card-text>
        <div class="overlay">
          <div class="text">
            Termasuk dalam <br />zona <span>Orange</span> covid-19
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
  props: {
    all: {
      type: Object,
      default: () => {},
    },
  },
  // props: {
  //   popular: {
  //     type: Object,
  //     default: () => {}
  //   }
  // }
};
</script>

<style scoped>
.bottom-right {
  position: absolute;
  bottom: 8px;
  right: 16px;
}
.bottom-right p {
  font-size: 20px;
}
.bottom-right svg {
  color: #FFD700;
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