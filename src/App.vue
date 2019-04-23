<template>
  <div id="app">
    <Header/>
    <Longread/>
    <Footer/>
  </div>
</template>

<script>
import Longread from './Longread.vue'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Longread,
    Header,
    Footer
  }
}
</script>

<style>
#app {
  font-family: 'Gotham Pro', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color:#ffffff;
  width: 100%;
  margin: 0 auto;
  width: 1024px;
  box-shadow: 0 0 10px rgba(0,0,0,0.5);
}
body {
  margin: 0;
}
</style>
