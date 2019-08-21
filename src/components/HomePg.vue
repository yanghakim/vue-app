<template>
  <div class="homePg">
    <transition name="heading">
      <Heading v-if="show" />
    </transition>

    <transition name="sections">
      <Sections v-if="!show" />
    </transition>

    <p
      class="homePg-extendBtn"
      v-bind:class="{ expand: show, back: !show }"
      v-on:click="navBtnToggle()"
    >
      {{ navBtnText }}
    </p>

    <div class="homePg__graphic">
      <img
        class="homePg__graphic-img"
        src="../assets/heart.jpg"
        v-bind:class="{ expand: !show, shrink: show }"
      />
      <div class="homePg__graphic__testimonial">
        <p class="homePg__graphic__testimonial-quote">
          “Our department tripled our productivity and I am confident we are
          producing standards-compliant structured reports that are concise,
          accurate and immediately available to referring physicians.”
        </p>
        <p class="homePg__graphic__testimonial-btn">
          Read Testimonials
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import Heading from "./HomePg/Heading.vue";
import Sections from "./HomePg/Sections.vue";

export default {
  name: "HomePg",
  components: {
    Heading,
    Sections
  },
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
      this.$emit("expanded", this.show);
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

@keyframes enterLeft
  0%
    transform: translateX(-500%)
  100%
    transform: translateX(0)

@keyframes exitLeft
  0%
    transform: translateX(0)
  100%
    transform: translateX(-500%)

@keyframes expandLeft
  0%

  50%
    filter: brightness(1)
    right: 0

  100%
    filter: brightness(0.4)
    transform: scale(1.2)
    right: 0

@keyframes shrinkRight
  0%
    filter: brightness(0.4)
    transform: scale(1.2)
    right: 0
  50%
    filter: brightness(1)
    right: 0

  100%
    right: -15%

.heading-enter-active
  animation: enterLeft 1s

.heading-leave-active
  animation: exitLeft 1s

.sections-enter-active
  animation: fadeIn 2s

.sections-leave-active
  animation: fadeOut 0.5s

.homePg
  width: 100vw
  height: 100%

  display: flex
  flex-direction: row
  align-items: center

  &-extendBtn
    position: absolute
    bottom: 10%
    left: 10vw

    padding-left: 5px

    cursor: pointer
    transition: 0.5s ease

    &.expand
      border-left: 2px solid white
      &:hover
        border-left: 2px solid red
        color: red

    &.back
      color: white
      border: 1px solid white
      padding: 5px 10px

      border-radius: 20px
      &:hover
        color: red
        border: 1px solid red

  &__graphic
    z-index: -1
    height: 100%

    &-img
      position: fixed
      top: -10%
      right: -15%

      &.expand
        animation: expandLeft 1s ease forwards

      &.shrink
        animation: shrinkRight 1s ease forwards

    &__testimonial
      position: absolute
      width: 30%
      right: 5%
      bottom: 5%

      display: flex
      flex-direction: column
      align-items: flex-end

      &-quote
        color: white
        padding: 10px
        text-align: right

        margin-top: 10px

      &-btn
        padding: 10px
        background: none
        color: white

        margin-top: 10px

        border: 1px solid white
        border-radius: 20px

        cursor: pointer
        transition: 0.5s ease
</style>
