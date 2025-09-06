<template>
   <div class="infoComposta-container">
    <ControlComRead />
  </div>
</template>

<script>
import ControlComRead from './ControlComRead.vue';

export default {
  name: 'ControlComposta',
  components:{
    ControlComRead
  }
};
</script>

<style scoped>
.infoComposta-container {
  padding: 0 10px;
  max-width: 1000px;
  min-width: 200px;
  margin: auto;
  font-family: sans-serif;
  line-height: 1.6;
  font-size: medium;
  text-align: justify;
}

</style>