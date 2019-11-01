<template>
  <div id="app">
    <KonvaTest></KonvaTest>
  </div>
</template>

<script>
  import KonvaTest from './components/KonvaTest.vue'

  export default {
  name: 'app',
  components: {
    KonvaTest
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
