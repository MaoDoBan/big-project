<template>
  <h1>{{ projeto }}</h1><br>
  <Modal v-if="showModal" :modal="modal" tema="azul" @toggle="toggleModal"/>
  <button @click="toggleModal">Mostrar Modal</button>
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
        título: "Nada para ver aqui",
        texto:  "Vá embora!"
      },
      showModal: false
    };
  },
  methods: {
    toggleModal(){
      this.showModal = !this.showModal;
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
#app h1{
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
