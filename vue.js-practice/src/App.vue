<template>
<div>
  <img alt="Vue logo" src="./assets/logo.png">
  <Home/>
</div> 
</template>

<script>
import Home from './components/Home.vue'

export default {
  name: 'App',
  data () {
    return{
      api_key: 'd5e4d419a18fabbf6f39acd494c88391'
    }
  },
  components: {
    Home
  }
}
</script>

<!--CSS stuff-->
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
