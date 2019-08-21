<template>
  <div class="homePg">
    <transition name="fade">
      <div class="homePg__heading" v-if="show">
        <p class="homePg__heading-header">Cardiovascular Information System</p>
        <p class="homePg__heading-subtitle">
          The Fastest Way to Create and Manage Medical Information
        </p>
        <div class="homePg__heading__btns">
          <p class="homePg__heading__btns-btn accent">Schedule a demo</p>
          <p class="homePg__heading__btns-btn">Call us at 800 399-7035</p>
        </div>
      </div>
    </transition>

    <p class="homePg__heading-extendBtn" v-on:click="navBtnToggle()">
      {{ navBtnText }}
    </p>

    <div class="homePg__graphic">
      <img
        class="homePg__graphic-img"
        src="../assets/heart.jpg"
        v-bind:class="{ expand: !show, shrink: show }"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "HomePg",
  data() {
    return {
      show: true,
      navBtnText: "view more"
    };
  },
  methods: {
    navBtnToggle: function() {
      this.show = !this.show;
      if (this.navBtnText === "view more") {
        this.navBtnText = "return to home";
      } else {
        this.navBtnText = "view more";
      }
    }
  }
};
</script>

<style lang="sass">
@keyframes fadeIn
  0%
    opacity: 0
  100%
    opacity: 1

@keyframes fadeOut
  0%
    opacity: 1
  100%
    opacity: 0

@keyframes expandLeft
  0%

  50%
    filter: blur(0px)
    right: 0

  100%
    filter: blur(3px)
    transform: scale(1.2)
    right: 0

@keyframes shrinkRight
  0%
    filter: blur(3px)
    transform: scale(1.2)
    right: 0
  50%
    filter: blur(0px)
    right: 0

  100%
    right: -15%

.fade-enter-active
  animation: fadeIn 0.5s ease

.fade-leave-active
  animation: fadeOut 0.5s ease

.homePg
  width: 100vw
  height: 100vh


  display: flex
  flex-direction: row
  align-items: center

  &__heading
    display: flex
    flex-direction: column
    justify-content: center

    height: 100%

    padding-left: 10vw
    padding-right: 5vw

    background: white

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
      left: 10vw

      border-left: 2px solid black
      padding-left: 5px

      cursor: pointer
      transition: 0.5s ease

      &:hover
        border-left: 2px solid red
        color: red

  &__graphic
    z-index: -2
    &-img
      position: fixed
      top: -10%
      right: -15%

      &.expand
        animation: expandLeft 1s ease forwards

      &.shrink
        animation: shrinkRight 1s ease forwards
</style>
