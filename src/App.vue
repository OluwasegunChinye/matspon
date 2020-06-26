<template>
  <div id="app">
    <Home />
  </div>
</template>

<script>
import Home from './components/Home.vue'


export default {
  name: 'App',
  components: {
    Home
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Ubuntu&display=swap');

#app {
  font-family: 'Ubuntu', sans-serif;
  
}

body{
  margin: 0;
}
</style>
