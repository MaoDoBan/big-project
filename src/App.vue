<template>
  <h1>{{ projeto }}</h1><br>
  <teleport to="#modal-aqui">
    <Modal v-if="showModal" tema="azul" @toggle="toggleModal">
      <h1>{{ modal.título }}</h1>
      <p> {{ modal.texto }}</p>
      <template v-slot:bah>
        <a href="#">BAH</a>
      </template>
    </Modal>
  </teleport>
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
#app, #modal-aqui{
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
