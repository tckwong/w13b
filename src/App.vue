<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <VueTweets></VueTweets>
  </div>
</template>

<script>
import VueTweets from './components/MyTweets'

export default {
  name: 'App',
  components: {
    VueTweets
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
