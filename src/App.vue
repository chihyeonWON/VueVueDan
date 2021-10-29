<template>
  <div id="root">
    <div>
      {{ first }} 곱하기 {{ second }} 는?
    </div>
    <form>
      <input type="number">
      <button>입력</button>
    </form>
  </div>
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
