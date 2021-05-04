<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <HadithWorld :items="items" msg="হাদিস"/>
</template>

<script>
import HadithWorld from './components/HadithWorld'

export default {
  name: 'App',
  components: {
    HadithWorld
  },
  data() {
    return {
      items: []
    }
  },
  mounted() {
    fetch('https://bn-hadith-api.herokuapp.com/hadiths')
    .then(response => response.json())
    .then(data => {
      this.items = data;
    });
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 30px 0;
}
</style>
