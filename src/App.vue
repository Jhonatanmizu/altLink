<script setup>
import Item from "./components/Item.vue";
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
</script>

<script>
import date from "./data/Services.json";
export default {
  data() {
    return {
      services: null,
    };
  },
  mounted() {
    // console.log(date);
    this.services = date;
  },
};
</script>
<template>
  <div class="main-container">
    <img
      class="main-image"
      alt="Jhonatan Jesus"
      src="https://avatars.githubusercontent.com/u/61719180?s=400&u=06b559d4e211817e13bb349ce04b562e5a12473e&v=4"
    />
    <h3 class="main-title">Jhonatan Jesus</h3>
    <span class="main-subtitle"> Frontend Developer JS | VUE | ANGULAR</span>
  </div>
  <div class="separator"></div>
  <div class="items-container fadeInDownBig">
    <Item v-for="(service, index) in services" :key="index" :item="service" />
  </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
a {
  text-decoration: none;
}
li {
  list-style: none;
}
html {
  font-size: 62.5%;
}
body {
  margin: 0 auto;
  font-family: "Montserrat", sans-serif;
  font-size: 1rem;
  background-color: #181b28;
  background-image: url("data:image/svg+xml,%3Csvg width='6' height='6' viewBox='0 0 6 6' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='%23005481' fill-opacity='0.4' fill-rule='evenodd'%3E%3Cpath d='M5 0h1L0 6V5zM6 5v1H5z'/%3E%3C/g%3E%3C/svg%3E");
  color: #f8f8f8;
}
.main-container {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  gap: 1rem;
  margin: 1rem;
}
.main-container .main-title {
  font-size: 2rem;
}
.main-container .main-title:hover {
  color: #14c8fe;
}
.main-container .main-subtitle {
  font-size: 1.6rem;
  font-weight: 300;
}
.main-container .main-image {
  height: 20rem;
  width: 20rem;
  border-radius: 100%;
  border: solid 3px #14c8fe;
}
.items-container {
  display: grid;
  grid-template-rows: 1fr;
  grid-template-columns: 1fr 1fr 1fr 1fr;
}
.separator {
  height: 2px;
  min-width: 100%;
  background: #14c8fe;
}
.fadeInDownBig {
  -webkit-animation-name: fadeInDownBig;
  animation-name: fadeInDownBig;
  -webkit-animation-duration: 1s;
  animation-duration: 1s;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
}
@-webkit-keyframes fadeInDownBig {
  0% {
    opacity: 0;
    -webkit-transform: translate3d(0, -2000px, 0);
    transform: translate3d(0, -2000px, 0);
  }
  100% {
    opacity: 1;
    -webkit-transform: none;
    transform: none;
  }
}
@keyframes fadeInDownBig {
  0% {
    opacity: 0;
    -webkit-transform: translate3d(0, -2000px, 0);
    transform: translate3d(0, -2000px, 0);
  }
  100% {
    opacity: 1;
    -webkit-transform: none;
    transform: none;
  }
}
@media (max-width: 800px) {
  .items-container {
    display: grid;
    grid-template-rows: 1fr 1fr 1fr 1fr;
    grid-template-columns: 1fr;
  }
}
</style>
