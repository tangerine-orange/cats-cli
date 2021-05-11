<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <MetamaskLogin msg="Login using Metamask"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import MetamaskLogin from './components/MetamaskLogin.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    MetamaskLogin
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
