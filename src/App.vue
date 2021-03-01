<template>
  <div id="app">
    <div>
      {{ info }}
    </div>
    <hello-world :editable="editable" :info.sync="info"></hello-world>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  data () {
    return {
      editable: 'edit',
      info: 'my demo'
    }
  },
  components: {
    HelloWorld
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
