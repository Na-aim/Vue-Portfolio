<template>
  <Navbar/>
  <Sections/>
  <Footer/>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Sections from './components/Sections.vue'
import Footer from './components/Footer.vue'
export default {
  name: 'App',
  components: {
    Navbar,Sections,Footer
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
</style>
