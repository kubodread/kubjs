<template>
  <div class="tutorial-container">
    <ControlCompostaRead />
  </div>
</template>

<script>
// Importa el archivo .md como un componente
import ControlCompostaRead from './ControlComRead.md';

export default {
  name: 'ControlC',
  components: {
    // Registra el componente para que pueda ser usado en la plantilla
    ControlCompostaRead,
  },
};
</script>

<style scoped>
/* Opcional: Estilos para el contenedor de tu tutorial */
.tutorial-container {
  padding: 20px;
  max-width: 800px;
  margin: auto;
  font-family: sans-serif;
  line-height: 1.6;
}
</style>
