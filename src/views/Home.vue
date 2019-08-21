<template>
  <div class="home">
    <Header v-bind:expanded="show" />
    <Nav v-bind:expanded="show" />
    <HomePg @expanded="onExpandToggle" />
  </div>
</template>

<script>
import Nav from "../components/Nav.vue";
import Header from "../components/Header.vue";
import HomePg from "../components/HomePg.vue";

export default {
  name: "Home",
  components: {
    Nav,
    Header,
    HomePg
  },
  data() {
    return {
      show: null
    };
  },
  methods: {
    onExpandToggle(value) {
      this.show = value;
    }
  }
};
</script>

<style lang="sass">
.home
  width: 100vw
  height: 100vh

  display: flex
  justify-content: center
  align-items: center

  overflow-x: hidden
</style>
