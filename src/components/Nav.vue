<template>
  <div class="nav" v-bind:class="{ black: expanded, white: !expanded }">
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
  name: "Nav",
  props: ["expanded"]
};
</script>

<style lang="sass">
@import url('https://fonts.googleapis.com/css?family=Raleway:400,900|Roboto:300&display=swap')

.nav
  position: absolute
  right: 5%
  top: 40px
  padding: 5px 15px

  display: flex
  flex-direction: row
  align-items: center

  z-index: 2

  @media (max-width: 600px)
    justify-content: center
    right: auto

  &.white
    color: white

  &.black
    color: black

  &-icon
    font-size: 2em
    cursor: pointer

    transition: 0.5s ease
    display: none

    @media (max-width: 600px)
      display: block

    &:hover
      color: red

  &-item
    margin: 0 20px
    cursor: pointer
    transition: 0.5s ease

    @media (max-width: 600px)
      margin: 0 5px

    &:hover
      color: red

    &.homepg
      color: red

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
