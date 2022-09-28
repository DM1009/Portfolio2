<template>
  <home />
  <about />
  <skill />
</template>

<script>
import home from './components/PFHome.vue'
import about from './components/PFAbout.vue'
import skill from './components/PFSkill.vue'
export default {
  name: 'App',
  components: {
    home, about, skill
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
