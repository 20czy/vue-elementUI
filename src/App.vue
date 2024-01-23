<template>
  <div id="app">
    <HelloWorld></HelloWorld>
    <TimeTable></TimeTable>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TimeTable from './components/TimeTable.vue';
export default {
  name: 'App',
  components: {
    HelloWorld,
    TimeTable
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
