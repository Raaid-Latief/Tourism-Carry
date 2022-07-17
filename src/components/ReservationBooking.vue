<template>
  <div>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <h1 class="booking-head text-danger display-2">Reservation Bookings</h1>
    <h5>Reservation Details</h5>
    <form action="https://formspree.io/f/mvoljqra" method="POST">
      <div class="row">
        <div class="col-md-6">
          <label>
            First Name
            <input class="form-control" type="text" name="name" required />
          </label>
        </div>
        <div class="col-md-6">
          <label>
            Last Name
            <input class="form-control" type="text" name="name" required />
          </label>
        </div>
        <div class="col-md-6">
          <label>
            Phone
            <input class="form-control" type="text" name="phone" required />
          </label>
        </div>
        <div class="col-md-6">
          <label>
            Email
            <input class="form-control" type="text" name="email" required />
          </label>
        </div>
        <div class="city">
          <label>
            City
            <select v-model="area" id="" class="form-control" type="" name="">
              <option value="All">All</option>
              <option value="Cape Town">Cape Town</option>
              <option value="Durban">Durban</option>
              <option value="Pretoria">Pretoria</option>
            </select>
          </label>
        </div>
        <div class="col-md-3">
          <label>
            Check-in Date
            <input class="form-control" type="date" name="date" required />
          </label>
        </div>
        <div class="col-md-3">
          <label>
            Check-in Time
            <input class="form-control" type="time" name="time" required />
          </label>
        </div>
        <div class="col-md-3">
          <label>
            Check-out Date
            <input class="form-control" type="date" name="date" required />
          </label>
        </div>
        <div class="col-md-3">
          <label>
            Check-out Time
            <input class="form-control" type="time" name="time" required />
          </label>
        </div>
        <div class="col-md-6">
          <label>
            Number of adults
            <input class="form-control" type="number" name="number" required />
          </label>
        </div>
        <div class="col-md-6">
          <label>
            Number of children
            <input class="form-control" type="number" name="number" required />
          </label>
        </div>
        <div class="p-5">
<button class="button" style="vertical-align:middle"><span>Book now</span></button>
</div>
      </div>
    </form>
  </div>
</template>
<script>
export default {};
</script>
<style>
input.form-control {
  width: 15rem;
}

.col-md-6 {
  padding-top: 2rem;
}
.col-md-3 {
  padding-top: 2rem;
  display: flex;
  /* padding-left: 54px; */
}
div#app {
  padding-left: 5rem;
  padding-right: 5rem;
}
/* media queries */
@media only screen and (max-width: 904px) {
  .col-md-3 {
    display: flex;
    justify-content: center;
  }
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









