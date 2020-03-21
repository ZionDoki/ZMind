<template>
  <div id="app">
    <ZMind />
  </div>
</template>

<script>
import ZMind from './components/ZMind'

export default {
  name: 'App',
  components: {
    ZMind
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
