<template>
  <section id="Home"><Home/></section>
  <section id="About"><About/></section>
  <section id="Resume"><Resume/></section>
  <section id="Skills"><Skills/></section>
  <section id="Projects"><Projects/></section>
  <section id="Testimonals"><Testimonals/></section>
  <section id="Contact"><Contact/></section>
</template>

<script>
import Home from '../components/Home.vue'
import About from '../components/About.vue'
import Resume from '../components/Resume.vue'
import Skills from '../components/Skills.vue'
import Projects from '../components/Projects.vue'
import Testimonals from '../components/Testimonals.vue'
import Contact from '../components/Contact.vue'
export default {
    components: {
        Home,
        About,
        Resume,
        Skills,
        Projects,
        Testimonals,
        Contact
    }

}
</script>

<style>

</style>