<template>
  <div id="app">
    <Button />
    <Quote />
  </div>
</template>

<script>
import Quote from './components/Quote.vue'
import Button from './components/Button.vue'


export default {
  name: 'App',
  components: {
    Quote,
    Button
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
