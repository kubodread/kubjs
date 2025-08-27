<template>
  
        <h2>¡Bienvenido!</h2>
        <p>Como profesional en gestión ambiental, mi misión es promover el desarrollo sostenible.
        <br><br>
         A través de la aplicación de herramientas y estrategias especializadas, ofrezco soluciones 
         que generan un impacto positivo en el entorno y la sociedad. 
         <br> <br>
         Mi trabajo se enfoca en:
         <ul>
         <li>
          Asesoramiento estratégico
         </li>
         
         <li>
          Gestión de proyectos sostenibles
         </li>
         <li>
          Capacitación y educación ambiental
         </li>
         </ul>
         </p>

</template>

<script>
export default {
  name: 'modalBienvenida',  
   props: {
    claseContenedor: {
      type: String,
      required: true
    }
  }
}
</script>