<template>
  <div id="app">
    <com-header v-bind:titleHeader="title" v-on:AppChangeTitle="handleChangeTitle"/>
    <img src="./assets/logo.png">
    <h1>{{ msg }}</h1>
    <com-list-user v-bind:listUsers="users"/>
    <com-footer v-bind:titleFooter="title"/>
  </div>
</template>

<script> 
import ComHeader from './components/ComHeader.vue';
import ComListUser from './components/ComListUser.vue';
import ComFooter from './components/ComFooter.vue';
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to My Projet',
      users: [
            {
                name: 'phi',
                age: 20
            },
            {
                name: 'dao',
                age: 22
            },
            {
                name: 'van',
                age: 21
            }
        ],
    title: 'my title'
    }
  },
  methods: {
handleChangeTitle(e) {
  this.title = e;
}
  },
  components: {
    ComHeader,
    ComFooter,
    ComListUser
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
