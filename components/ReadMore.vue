<template>

  <div class="">

    <div class="btn-more" v-on:click="show = !show">
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
  }
}
</script>

<style scoped lang="scss">

.fade-enter-active, .fade-leave-active {
  transition: all 0.3s;
}

.fade-enter, .fade-leave-to {
  transform: scale(0.05);
  opacity: 0;
}
</style>