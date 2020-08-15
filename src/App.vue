<template>
  <div id="app">
    <com-header></com-header>
    <img src="./assets/logo.png">
    <h1>{{ msg }}</h1>
    <com-footer></com-footer>
  </div>
</template>

<script> 
import ComHeader from './components/ComHeader';
import ComFooter from './components/ComFooter';
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to My Projet'
    }
  },
  components: {
    ComHeader,
    ComFooter
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
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
