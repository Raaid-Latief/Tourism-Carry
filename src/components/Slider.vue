<template>
<section id="about">
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>

    <h1 class="text-danger p-4 text-danger display-1">Take a tour with us</h1>

<div>
  <div class="carousel">
    <ul class="slides">
      <input type="radio" name="radio-buttons" id="img-1" checked />
      <li class="slide-container">
        <div class="slide-image">
         <img src="https://i.postimg.cc/B6P68MQW/table-mountain.jpg">
      <div class="carousel-caption d-none d-md-block">
    <h2 class="display-2 text-warning">Cape Town</h2>
 
  </div>
      </div>
        <div class="carousel-controls">
          <label for="img-3" class="prev-slide">
            <span>&lsaquo;</span>
          </label>
          <label for="img-2" class="next-slide">
            <span>&rsaquo;</span>
          </label>
        </div>
      </li>
      <input type="radio" name="radio-buttons" id="img-2" />
      <li class="slide-container">
        <div class="slide-image">
         <img src="https://i.postimg.cc/02M6M5jM/1571854466-32849.jpg"> 
       <div class="carousel-caption d-none d-md-block">
    <h2 class="display-2 text-warning">Durban</h2>

      </div>
      </div>  
        <div class="carousel-controls">
          <label for="img-1" class="prev-slide">
            <span>&lsaquo;</span>
          </label>
          <label for="img-3" class="next-slide">
            <span>&rsaquo;</span>
          </label>
        </div>
      </li>
      <input type="radio" name="radio-buttons" id="img-3" />
      <li class="slide-container">
        <div class="slide-image">
          <img src="https://i.postimg.cc/j2NL1vG6/union-buildings.jpg">
      <div class="carousel-caption d-none d-md-block">
    <h2 class="display-2 text-warning">Pretoria</h2>

      </div>
      </div>
        <div class="carousel-controls">
          <label for="img-2" class="prev-slide">
            <span>&lsaquo;</span>
          </label>
          <label for="img-4" class="next-slide">
            <span>&rsaquo;</span>
          </label>
        </div>
      </li>
      <input type="radio" name="radio-buttons" id="img-4" />
      <li class="slide-container">
        <div class="slide-image">
         <img src="https://i.postimg.cc/xTvXyxGn/The-Big-Hole-1.jpg"> 
       <div class="carousel-caption d-none d-md-block">
    <h2 class="display-2 text-warning">Kimberely</h2>
   
      </div>
      </div>  
        <div class="carousel-controls">
          <label for="img-3" class="prev-slide">
            <span>&lsaquo;</span>
          </label>
          <label for="img-1" class="next-slide">
            <span>&rsaquo;</span>
          </label>
        </div>
      </li>
      <div class="carousel-dots">
        <label for="img-1" class="carousel-dot" id="img-dot-1"></label>
        <label for="img-2" class="carousel-dot" id="img-dot-2"></label>
        <label for="img-3" class="carousel-dot" id="img-dot-3"></label>
        <label for="img-4" class="carousel-dot" id="img-dot-4"></label>
      </div>
    </ul>
  </div>
</div>
<div class="p-5">
<button class="button" style="vertical-align:middle"><span>Book a tour now !</span></button>
</div>

</section>
</template>
<script>
export default {
    name: 'Slider'
}
</script>
<style>
    * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}
/* .page{
     background-image: linear-gradient(to right top, #002762, #4e226d, #840666, #ae004e, #c60629);
} */
h2{
    color: #00000086;
     position: relative;
  bottom: 50px;
 font-style: normal;
 font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
}
.carousel {
    margin-left: 15%;
    margin-right: 15%;
}

ul.slides {
    display: block;
    position: relative;
    height: 600px;
    margin: 0;
    padding: 0;
    overflow: hidden;
    list-style: none;
}

.slides * {
    user-select: none;
    -ms-user-select: none;
    -moz-user-select: none;
    -khtml-user-select: none;
    -webkit-user-select: none;
    -webkit-touch-callout: none;
}

ul.slides input {
    display: none; 
}


.slide-container { 
    display: block; 
}

.slide-image {
    display: block;
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    opacity: 0;
    transition: all .7s ease-in-out;
}   

.slide-image img {
    width: auto;
    min-width: 100%;
    height: 100%;
}

.carousel-controls {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    z-index: 999;
    font-size: 100px;
    line-height: 600px;
    color: #fff;
}

.carousel-controls label {
    display: none;
    position: absolute;
    padding: 0 20px;
    opacity: 0;
    transition: opacity .2s;
    cursor: pointer;
}

.slide-image:hover + .carousel-controls label{
    opacity: 0.5;
}

.carousel-controls label:hover {
    opacity: 1;
}

.carousel-controls .prev-slide {
    width: 49%;
    text-align: left;
    left: 0;
}

.carousel-controls .next-slide {
    width: 49%;
    text-align: right;
    right: 0;
}

.carousel-dots {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 20px;
    z-index: 999;
    text-align: center;
}

.carousel-dots .carousel-dot {
    display: inline-block;
    width: 30px;
    height: 30px;
    border-radius: 50%;
    background-color: #fff;
    opacity: 0.5;
    margin: 10px;
}

input:checked + .slide-container .slide-image {
    opacity: 1;
    transform: scale(1);
    transition: opacity 1s ease-in-out;
}

input:checked + .slide-container .carousel-controls label {
     display: block; 
}

input#img-1:checked ~ .carousel-dots label#img-dot-1,
input#img-2:checked ~ .carousel-dots label#img-dot-2,
input#img-3:checked ~ .carousel-dots label#img-dot-3,
input#img-4:checked ~ .carousel-dots label#img-dot-4,
input#img-5:checked ~ .carousel-dots label#img-dot-5,
input#img-6:checked ~ .carousel-dots label#img-dot-6 {
	opacity: 1;
}


input:checked + .slide-container .nav label { display: block; }

body, html {
  padding: 0;
  margin: 0;
  width: 100%;
  min-height: 100vh;
}
body {
     background-image: linear-gradient(to right top, #002762, #4e226d, #840666, #ae004e, #c60629);
}


/* button */
.button {
  display: inline-block;
  border-radius: 4px;
background-image: linear-gradient(to right bottom, #000062, #65006a, #a70062, #db004e, #ff002e);
  border: none;
  color: #FFFFFF;
  text-align: center;
  font-size: 15px;
  padding: 20px;
  width: 150px;
  height: 80px;
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
</style>






