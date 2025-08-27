<template>
  <div :class="claseContenedor">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'ArticuloNota',
  props: {
    claseContenedor: {
      type: String,
      required: true
    }
  }
}

</script>

<style scoped>

.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.7);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 100;
}

.modal-content {
  background: white;
  padding: 30px;
  border-radius: 10px;
  text-align: center;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
}
/* Aquí puedes agregar estilos base para el componente si lo necesitas */
</style>