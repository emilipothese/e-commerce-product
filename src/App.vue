<template>
  <section class="container">
    <nav-bar></nav-bar>
    <product-view></product-view>
  </section>
</template>

<script>
import NavBar from './components/NavBar.vue'
import ProductView from './components/ProductView.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    ProductView
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.container {
  width: 900px;
  margin: 0 auto;
}

@media screen and (max-width: 900px) {
  .container {
    width: 375px;
    margin: 0 auto;
  }
}
</style>
