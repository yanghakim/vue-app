<template>
  <div class="header">
    <img class="header-logo" src="../assets/logo.png" />
    <p
      class="header-title"
      v-bind:class="{ black: expanded, white: !expanded }"
    >
      EncaptureMD
    </p>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: ["expanded"]
};
</script>

<style lang="sass">
@import url('https://fonts.googleapis.com/css?family=Raleway&display=swap')

.header
  position: absolute
  left: 10%
  top: 40px

  height: 40px

  display: flex
  flex-direction: row
  align-items: center

  z-index: 5

  &-title
    font-size: 1.5em

    font-family: 'Raleway', sans-serif

    &.white
      color: white

    &.black
      color: black

  &-logo
    width: 40px
    height: 40px

    margin-top: 5px
    margin-right: 10px
</style>
