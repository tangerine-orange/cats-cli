<template>
<div class="fluid-container sticky-top">
<b-navbar variant="faded" type="light">
    <b-navbar-brand class="ml-auto" href="#">
      <img :src="require('../../assets/CATS.png')" alt="" width="140" height="80"/>
      <a font-weight= "900"> C.A.T.S</a>
    </b-navbar-brand>
    
    <b-navbar-button class="col"> 
         <li>{{ msg }}</li>
         <button v-on:click="greet" class="enableEthereumButton">Connect</button>
      </b-navbar-button>
</b-navbar>
</div>

</template>

<script>

if (typeof window.ethereum !== 'undefined') {
  console.log('MetaMask is installed!');
}

export default {
  name: 'MetamaskLogin',
  props: {
    msg: String
  },
  methods: {
    greet: () => {
      window.ethereum.request({ method: 'eth_requestAccounts' });
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  font-family: "Exo", weight 100;
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>


