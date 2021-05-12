<template>

<div>
  <sticky-header/>
  <div>
  </div>
    <footer/>
  </div>
  
  <MetamaskLogin msg="Login using Metamask"/>
</template>

<script>

import StickyHeader from './components/Header-Footer/Header.vue'

export default {
  name: 'App',
  components: {
    StickyHeader

  }
}

</script>

<style>
#app {
  font-family: 'Exo', 'Helvetica', 'Arial', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
