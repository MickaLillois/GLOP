<template>
  <div id="app">
    <CommonTop/>
    <Nav />
    <!-- !PAGE CONTENT! -->
    <div class="w3-main" style="margin-left:300px;margin-top:43px;">
      <router-view />  
    </div>
    <Footer/>
  </div>
</template>

<script>
import CommonTop from './components/CommonTop.vue'
import Nav from './components/Nav.vue'
import Footer from './components/Footer.vue'
export default {
  name: 'App',
  components: {
    CommonTop,
    Nav,
    Footer
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
