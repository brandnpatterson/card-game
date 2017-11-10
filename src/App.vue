<template>
  <div id="app">
    <img src="./assets/logo.png">
    <CardGame/>
  </div>
</template>

<script>
import CardGame from './components/CardGame'

export default {
  name: 'app',
  components: {
    CardGame
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
