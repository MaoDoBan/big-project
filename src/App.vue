<template>
  <h1>{{ title }}</h1><br>
  <input type="text" ref="bah"><br>
  <button @click="clicaAqui">Clica aqui</button>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      title: "Big Project"
    };
  },
  methods: {
    clicaAqui(){
      this.$refs.bah.focus();
    }
  }
}
</script>

<style>
body{
  background-color: #999;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1{
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
