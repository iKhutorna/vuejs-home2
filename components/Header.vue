<template>

<div class="header">
     <div class="header__in">
        <div class="header__name">Classic</div>
        <div class="nav">
          <nuxt-link to="/">Home</nuxt-link>
          <nuxt-link to="/news">News</nuxt-link>

          <!-- <img src="@/assets/home.png">
          <router-link to="/">Home</router-link>
          <router-link to="/news">News</router-link> -->
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style lang="scss">
.header {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #fff;
  background: #000;
  &__name {
    font-weight: bold;
    color: #fff;
    font-size: 24px;
  }
  &__in {
    height: 80px;
    max-width: 975px;
    width: 945px;
    padding: 0 15px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}
.nav {
  //padding: 30px;
  a {
    font-weight: bold;
    color: #cccccc;
    font-size: 16px;
    margin-left: 32px;
    text-decoration: none;
    &:hover {
      text-decoration: underline;
    }
    text-transform: uppercase;
    &.router-link-exact-active {
      color: #fff;
      cursor: default;
      &:hover {
        text-decoration: none;
      }
    }
  }
}
</style>

