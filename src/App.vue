<template>
  <div id="app">
    <br/>
    <router-link to="/">Login</router-link> |
    <router-link to="/about">About</router-link>
    <!--<router-link to="/secure">Secure</router-link>
    <Header/> -->
  </div>
  <router-view />

</template>

<script>

//import Header from "@/components/Layout/Header.vue"

export default {
  name: "app",
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
  
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
