<template>
  <div id="root">
    <div>
      {{ first }} 곱하기 {{ second }} 는?
    </div>
    <form v-on:submit="onSubmitForm">
      <input type="number" v-model="inputValue" ref="answer">
      <button type="submit">입력</button>
    </form>
    <div id="result">
      {{result}}
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      first:Math.ceil(Math.random()*9),
      second:Math.ceil(Math.random()*9),
      inputValue:'',
      result:'',  
    }
  },
  methods: {
    onSubmitForm(e) {
      e.preventDefault(); // 버튼 눌렀을 때 새로고침되는 것을 방지
      // 첫번째 숫자와 두번째 숫자를 곱한 값이 입력한 숫자와 같을 때 정답을 출력 그렇지 않으면 땡을 출력
      if(this.first * this.second === parseInt(this.inputValue)) {
        this.result='정답';
        this.first = Math.ceil(Math.random() * 9);
        this.second = Math.ceil(Math.random() * 9);
        this.inputValue = '';
        // ref 속성으로 커서 깜빡임을 유지
        this.$refs.answer.focus();
      } else {
        this.result='오답';
        this.inputValue='';
      }
    },
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

</style>
