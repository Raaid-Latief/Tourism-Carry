<template>
  <div class="background">
     <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <div class="container shadow">
      <form @submit.prevent="login">
      <div>
         <h3 class="p-2 text-danger display-5">Admin Login</h3>
      </div>
        <input
          type="email"
          v-model="email"
          placeholder="enter your email"
          class="user_input p-1"
          required
        />
        <input
          type="password"
          v-model="password"
          placeholder="enter your password"
          class="user_input p-1"
          required
        />
        <div class="form_footer">
          <div><input type="checkbox" id="" /><label class="p-2">Remember Me</label></div>
          <a href="#" class="p-2">Forgot Password?</a>
        </div>
        <button
          type="submit"
          class="button rounded-pill mt-3"
          @click="goToAdmin">
          Login
        </button>
      </form>
     </div>
    </div>
</template>
<script>
export default {
  data() {
    return {
      email: "",
      password: "",
    };
  },
  computed: {
    user() {
      this.$store.state.user;
    },
  },
  methods: {
    Login() {
      this.$store.dispatch("login", {
        email: this.email,
        password: this.password,
      });
    },
    goToAdmin() {
      if (
        (this.email === "selbysabelomdashe@gmail.com" &&
          this.password === "password") ||
        (this.email === "natheerah24@gmail.com" &&
          this.password === "password") ||
        (this.email === "raaidlatiefgbr@gmail.com" &&
          this.password === "password") ||
        (this.email === "saliwalive@gmail.com" &&
          this.password === "password") ||
        (this.email === "json@gmail.com" && this.password === "password")
      ) {
        this.$router.push("/admin");
      } else {
        window.alert("Can't log you in.. Please check your login details");
      }
    },
  },
};
</script>
<style>
form {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.user_input {
  width: 300px;
  height: 30px;
  background-color: white;
}
.check {
  display: flex;
}
.container {
  display: flex;
  justify-content: center;
  margin-top: 30px;
  background-color: rgb(203, 253, 253);
  padding: 50px;
  width: fit-content;
}
.form_footer {
  display: flex;
  justify-content: space-between;
}
.button{
   padding: 15px 25px;
  font-size: 24px;
  text-align: center;
  cursor: pointer;
  outline: none;
  color: #fff;
  background-image: linear-gradient(to right top, #002762, #4e226d, #840666, #ae004e, #c60629);;
  border: none;
  border-radius: 9px;
  box-shadow: 0 9px #999;
}
.button:hover {background-image: linear-gradient(to right top, #420101, #2b0646, #4d043c, #e7247c, #36020c);}

.button:active {
  background-color: #464d46;
  box-shadow: 0 5px #666;
  transform: translateY(4px);
}
</style>














