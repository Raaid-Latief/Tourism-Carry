<template>
<section id="landing">
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <!-- <v-img
          :src="require('../assets/pexels-pixabay-259447.jpg')"
          class="my-5"
          contain
          height="100%"
          weight="100%"
        /> -->
      </v-col>
      <v-col class="mb-4">
        <div class="threeD">
        <h1 class="display-2 font-weight-bold mb-3">
          Welcome to South Africa
        </h1>
         </div>
  <div class="container d-flex justify-content-center align-item-center ">
    <div class="center">
      <button  class="btn" @click="goToAdmin">
        <svg width="180px" height="60px" viewBox="0 0 180 60" class="border">
          <polyline points="179,1 179,59 1,59 1,1 179,1" class="bg-line" />
          <polyline points="179,1 179,59 1,59 1,1 179,1" class="hl-line" />
        </svg>
        <span class="explore">Explore</span>
      </button>
    </div>
  </div>
      </v-col>
    </v-row>
  </v-container>
  </section>
</template>
<script>
export default {
  name: 'Landing',
  // data: () => ({
  // }),
}
</script>
<style scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}


.container {
  width: 400px;
  height: 400px;
  position: absolute;
  left: 50%;
  top: 70%;
  transform: translate(-50%, -50%);
  display: flex;
  justify-content: center;
  align-items: center;
}
.center {
  width: 180px;
  height: 60px;
  position: absolute;
}
.btn {
  width: 180px;
  height: 60px;
  cursor: pointer;
  background: transparent;
  outline: none;
  transition: 1s ease-in-out;
}
svg {
  position: absolute;
  left: 0;
  top: 0;
  fill-opacity: 35%;
  stroke: rgb(85, 11, 11);
  stroke-dasharray: 150 480;
  stroke-dashoffset: 150;
  transition: 1s ease-in-out;
}
.btn:hover {
  transition: 1s ease-in-out;
 background-image: linear-gradient(to right top, #002762, #4e226d, #840666, #ae004e, #c60629);
}
.btn:hover svg {
  stroke-dashoffset: -480;
}
.btn span {
  color: rgb(255, 255, 255);
  font-size: 28px;
 
}
#landing{
  background-image: url(https://i.im.ge/2022/07/08/ukwBGS.jpg);
  background-size: cover;
  background-position: center;
  min-height: 100vh;
 
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.threeD {
  color: darkgrey;
  white-space: nowrap;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 5em;
  font-family: sans-serif;
  letter-spacing: 0.1em;
  transition: 0.3s;
  text-shadow: 1px 1px 0 grey, 1px 2px 0 grey, 1px 3px 0 grey, 1px 4px 0 grey,
    1px 5px 0 grey, 1px 6px 0 grey, 1px 7px 0 grey, 1px 8px 0 grey,
    5px 13px 15px black;
}
.threeD:hover {
  transition: 0.3s;
  transform: scale(1.1)translate(-50%, -50%);
  text-shadow: 1px -1px 0 grey, 1px -2px 0 grey, 1px -3px 0 grey,
    1px -4px 0 grey, 1px -5px 0 grey, 1px -6px 0 grey, 1px -7px 0 grey,
    1px -8px 0 grey, 5px -13px 15px black, 5px -13px 25px #808080;
}
</style>










