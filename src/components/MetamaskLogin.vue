<template>
  <div class="login">
    <h1>{{ msg }}</h1>
    <button v-on:click="greet" class="enableEthereumButton">Enable Ethereum</button>
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
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
