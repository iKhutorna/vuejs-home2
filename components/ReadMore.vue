<template>

  <div class="">

    <!-- <div class="btn-more" v-on:click="show = !show">
      <div class="btn-more__icon">
        <img src="~assets/right-arrow.svg" alt="">
      </div>
      <div class="btn-more__text">Read more</div>
    </div>
    <div>
      <transition name="fade">
        <div v-if="show">
          <slot />
        </div>
      </transition>
    </div> -->

    <div class="element">

      <div class="btn-more" v-on:click="show = !show">
        <div class="btn-more__icon">
          <img src="~assets/right-arrow.svg" alt="">
        </div>
        <div class="btn-more__text">Read more</div>
      </div>
      
      <transition
        v-on:before-enter="beforeEnter"
        v-on:enter="enter"
        v-on:leave="leave"
        v-bind:css="false"
      >
        <div v-if="show">
          <slot />
        </div>
      </transition>

    </div>
  </div>

</template>

<script>
export default {
  transition: 'fade',
  data () {
    return {
      show: false
    }
  },
  methods: {
    beforeEnter: function (el) {
      el.style.opacity = 0
    },
    enter: function (el, done) {
      Velocity(el, { opacity: 1, fontSize: '1.4em' }, { duration: 300 })
      Velocity(el, { fontSize: '1em' }, { complete: done })
    },
    leave: function (el, done) {
      Velocity(el, {
        translateX: '1000px', fontSize: '0.1em', opacity: 0 }, { complete: done })
    }
  }

}
</script>

<style scoped lang="scss">

// .fade-enter-active, .fade-leave-active {
//   transition: all 0.3s;
// }

// .fade-enter, .fade-leave-to {
//   transform: scale(0.05);
//   opacity: 0;
// }
</style>