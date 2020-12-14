<template>
  <div>
    <div class="card-group">
    <b-card
    overlay
    :img-src="all.image"
    :img-alt="all.title"
    text-variant="info"
    :title="all.name"
    :sub-title="all.address"
  >
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