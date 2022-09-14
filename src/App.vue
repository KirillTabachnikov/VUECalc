<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Calc/>
  </div>
</template>

<script>
import Calc from './components/Calc';

export default {
  name: 'App',
  components: {
    Calc,
  },
  data() {
    return {
    };
  },
  methods: {
  },
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
