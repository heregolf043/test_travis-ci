<template>
  <div class="home">
    <br /><br />
    <h3>Welcome to my Vue.js App</h3> 
    <h4>by JUYNAG Team</h4>
    <img alt="Vue logo" src="../assets/logo.png" />
    <br /><br />
    UserName : <input type="text" name="username" v-model="input.username" />
    <br /><br />
    Password :
    <input type="password" name="password" v-model="input.password" />
    <br /><br />
    <button type="button" v-on:click="login()">Login</button>
    <button type="button" v-on:click="clear()">Clear</button>
    <br /><br />
  </div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: "Home",
  data() {
    return {
      title: "Login Page",
      uname: "",
      auth: 0,
      input: {
        username: "",
        password: "",
      },
    };
  },
  methods: {
    login() {
      if (this.input.username != "" && this.input.password != "") {
        this.uname = "Hello " + this.input.username;
        this.auth = 1;
        this.$router.push("Secure");
        //let routeData = this.$router.resolve({name: 'Secure', query: {data: this.uname}});
        // window.open(routeData.href, '_blank');
      } else {
        this.uname = "Please inut username and password";
      }
    },
    clear() {
      this.uname = "";
      this.input.username = "";
      this.input.password = "";
    },
  },
};
</script>
