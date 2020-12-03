<template>
    <router-view />
    <div id="secure">
        <h1>Hello World</h1>
        <p>
            Welcome to my Application
        </p>
        <!-- <button type="button" v-on:click="logout()">logout</button> -->
    </div>
    
</template>

<script>
    export default {
        name: 'Secure',
        data() {
            return {};
        },
        method:{
            logout(){
                this.$router.push("/");
            }
        }
    }
</script>

<style scoped>
    #secure {
        background-color: #FFFFFF;
        padding: 20px;
        margin-top: 10px;
    }
</style>