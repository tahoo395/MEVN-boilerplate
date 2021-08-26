<template>
  <p>This is the frontend part of Mevn stack {{lol}}</p>
</template>

<script>
import api from './api.js'

export default {
  data(){
    return {
      lol : ''
    }
  },
  async created(){
    let response = await api().get('/lol')
    this.lol = response.data.lol
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
