<template>
  <div class="nav">
    <p class="nav-item homepg">
      Home
    </p>
    <p class="nav-item">
      Modalities
    </p>
    <p class="nav-item">
      Modules
    </p>
    <p class="nav-item">
      Sales
    </p>
    <p class="nav-item">
      Support
    </p>
    <p class="nav-item loginpg">
      Login
    </p>
  </div>
</template>

<script>
export default {
  name: "Nav"
};
</script>

<style lang="sass">
@import url('https://fonts.googleapis.com/css?family=Raleway:400,900|Roboto:300&display=swap')

.nav
  position: absolute
  right: 10%
  top: 40px

  height: 40px

  display: flex
  flex-direction: row
  align-items: center

  z-index: 2

  &-item
    margin: 0 20px
    cursor: pointer
    transition: 0.5s ease

    color: black

    &:hover
      color: red

    &.homepg
      color: black

    &.loginpg
      border: 1px solid red
      padding: 5px 10px
      margin-left: 5px
      border-radius: 30px

      background-color: red
      color: white

      transition: 0.5s ease

      &:hover
        color: red
        background: none
</style>
