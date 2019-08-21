<template>
  <div class="heading">
    <p class="heading-header">Cardiovascular Information System</p>
    <p class="heading-subtitle">
      The Fastest Way to Create and Manage Medical Information
    </p>
    <div class="heading__btns">
      <p class="heading__btns-btn accent">Schedule a demo</p>
      <p class="heading__btns-btn">Call us at 800 399-7035</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Heading"
};
</script>

<style lang="sass">
.heading
  display: flex
  flex-direction: column
  justify-content: center

  height: 100%

  padding-left: 10vw
  padding-right: 5vw

  background: white

  @media (max-width: 1400px)
    padding: 0 10vw

  &-header
    font-family: "Raleway", sans-serif
    font-weight: 200
    letter-spacing: 1px
    font-size: 3em

    width: 500px

    @media (max-width: 1400px)
      width: 300px

  &-subtitle
    margin: 15px 5px
    padding: 5px 10px
    border-left: 2px solid red

  &__btns
    display: flex
    flex-direction: row

    &-btn
      padding: 10px
      border: 1px solid red
      width: auto

      margin-right: 20px

      border-radius: 20px
      color: red

      &.accent
        background: red
        color: white

        cursor: pointer
        transition: 0.5s ease

        &:hover
          color: red
          background: white
</style>
