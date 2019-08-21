<template>
  <div id="app">
    <Home />
  </div>
</template>

<script>
import Home from "./views/Home.vue";

export default {
  name: "app",
  components: {
    Home
  }
};
</script>

<style lang="sass">
@import url('https://fonts.googleapis.com/css?family=Raleway:200,400|Roboto:300&display=swap')
*
  padding: 0
  margin: 0
  box-sizing: border-box

  font-family: 'Roboto', sans-serif
</style>
