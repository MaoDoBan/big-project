<template>
  <div class="backdrop" @click.self="toggleModal">
    <div class="modal" :class="{ azul: tema === 'azul' }">
      <slot></slot>
      <div class="bah">
        <slot name="bah"></slot>
      </div>
    </div>
  </div>
</template>


<script>
export default{
  props: ["tema"],
  methods: {
    toggleModal(){
      this.$emit("toggle");
    }
  }
}
</script>


<style>
.modal{
  width: 400px;
  padding: 20px;
  margin: 100px auto;
  background: white;
  border-radius: 10px;
}
.modal.azul{
  background: darkblue;
}
.backdrop{
  top: 0;
  position: fixed;
  background: rgba(0, 0, 0, 0.5);
  width: 100%;
  height: 100%;
}
</style>