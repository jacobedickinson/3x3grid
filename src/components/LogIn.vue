<template>
  <div>
    <h4>Please enter credentials</h4>
    <h6>User & pass : "jacob"</h6>
    <img
      src="https://www.iconfinder.com/data/icons/iphone-black-people-svg-icons/20/login_user_profile_account_logout_people_man_human-512.png"
      alt
    />
    <br />
    <input type="text" v-model="user" placeholder="User" />
    <br />
    <input type="text" v-model="pass" placeholder="pass" />
    <br />

    <button @click="logInSuccessful">Log in</button>
    <p class="success">{{logInSuccess}}</p>
    <p class="fail">{{logInNotSuccess}}</p>
  </div>
</template>


<script>
export default {
  data() {
    return {
      user: "",
      pass: "",
      logInSuccess: "",
      logInNotSuccess: "",
    };
  },
  methods: {
    logInSuccessful() {
      if (this.user === "jacob" && this.pass === "jacob") {
        this.logInSuccess = "Log in successful";
        this.logInNotSuccess = "";
      } else {
        this.logInNotSuccess = "Log In unsuccessful";
        this.logInSuccess = "";
      }
    },
  },
};
</script>

<style scoped>
.button {
  width: 1000%;
}
img {
  height: 10em;
  width: auto;
}
div {
  margin: auto;
}
.fail {
  background-color: red;
}
.success {
  background-color: green;
}
</style>