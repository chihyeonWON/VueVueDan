<template>

</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      first:Math.ceil(Math.random()*9),
      second:Math.ceil(Math.random()*9),
    }
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
