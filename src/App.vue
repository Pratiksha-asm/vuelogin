<template>
  <div id="app">
   <h3>Task</h3>
   
   <router-view></router-view>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Login from './components/Login'
import Change from './components/Change'
export default {
  name: 'app',

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
