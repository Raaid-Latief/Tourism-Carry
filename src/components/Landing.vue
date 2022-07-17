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
 <button class="button" style="vertical-align:middle"><span>Explore </span></button>
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
.button {
  display: inline-block;
  border-radius: 4px;
background-image: linear-gradient(to right bottom, #000062, #65006a, #a70062, #db004e, #ff002e);
  border: none;
  color: #FFFFFF;
  text-align: center;
  font-size: 28px;
  padding: 18px;
  width: 200px;
  transition: all 0.5s;
  cursor: pointer;
  margin: 5px;
}

.button span {
  cursor: pointer;
  display: inline-block;
  position: relative;
  transition: 0.5s;
}

.button span:after {
  content: '\00bb';
  position: absolute;
  opacity: 0;
  top: 0;
  right: -20px;
  transition: 0.5s;
}

.button:hover span {
  padding-right: 25px;
}

.button:hover span:after {
  opacity: 1;
  right: 0;
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










