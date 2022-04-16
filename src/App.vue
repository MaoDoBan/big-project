<template>
  <h1>{{ projeto }}</h1><br>
  <Modal :titulo="modal.titulo" :texto="modal.texto"/>
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: 'App',
  components: { Modal },
  data(){
    return {
      projeto: "Big Project",
      modal: {
        titulo: "Nada para ver aqui",
        texto:  "Vá embora!"
      }
    };
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
#app h1{
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
