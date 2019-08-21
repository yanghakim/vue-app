<template>
  <div class="header">
    <img class="header-logo" src="../assets/logo.png" />
    <p class="header-title">EncaptureMD</p>
  </div>
</template>

<script>
export default {
  name: "Header"
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

  &-title
    font-size: 1.5em

    font-family: 'Raleway', sans-serif

  &-logo
    width: 40px
    height: 40px

    margin-top: 5px
    margin-right: 10px
</style>
