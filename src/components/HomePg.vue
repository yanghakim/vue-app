<template>
  <div class="homePg">
    <div class="homePg__heading">
      <p class="homePg__heading-header">Cardiovascular Information System</p>
      <p class="homePg__heading-subtitle">
        The Fastest Way to Create and Manage Medical Information
      </p>
      <div class="homePg__heading__btns">
        <p class="homePg__heading__btns-btn accent">Schedule a demo</p>
        <p class="homePg__heading__btns-btn">Call us at 800 399-7035</p>
      </div>

      <p class="homePg__heading-extendBtn">view more</p>
    </div>

    <div class="homePg__graphic">
      <img class="homePg__graphic-img" src="../assets/heart.jpg" />
    </div>
  </div>
</template>

<script>
export default {
  name: "HomePg"
};
</script>

<style lang="sass">
.homePg
  width: 100vw
  height: 100vh

  padding: 0 12%

  display: flex
  flex-direction: row
  align-items: center

  &__heading
    display: flex
    flex-direction: column
    justify-content: center

    &-header
      font-family: "Raleway", sans-serif
      font-weight: 200
      letter-spacing: 1px
      font-size: 3em

      width: 500px

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

    &-extendBtn
      position: absolute
      bottom: 5%

      border-left: 2px solid white
      padding-left: 5px

      cursor: pointer
      transition: 0.5s ease

      &:hover
        border-left: 2px solid red
        color: red

  &__graphic
    position: sticky
    &-img
      width: 2000px

      position: fixed
      top: -10%
</style>
