<template>
  <div>Hello world!</div>
  <members></members>
</template>

<script>
import Members from './components/Members.vue';
export default {
  name: 'App',
  components: {
    Members
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
  margin-top: 60px;
}
</style>
