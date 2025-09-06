<template>
  <div  class="contenedorK "> 
  <div class="contk1">
    <div class="">
    <img class="img1" alt="Vue logo" src='../assets/icon-512x512.png'>
      <h1>¡Bienvenido a Kubiotec!</h1>
    </div>
      <div class="">
        <article>
        Comprometido en encontrar soluciones adecuadas, innovadoras y eficientes, cumpliendo con las normas para cuidar y proteger nuestro planeta.
        <br><br><br>
        </article>
      </div>
  </div>

<div class="contk1">
                <div class="inicioEntrada">
                <article>
                    <h1>
                       &#128198; &#128209; Monitorea tu composta con esta app 	&#128200;&#128201;&#128202;
                    </h1>
                      <article>
                        <h2>Controla el progreso de tu composta</h2>
                        <i>Con esta app puedes registrar y monitorear diariamente o visualizar datos que tengas.</i> <br>
                        <i>Puedes importar y exportar archivos CSV para visualizar o procesar los datos</i>
                        Mira las siguientes capturas de pantalla de la aplicación. <br>
                      </article>
                      <h4>Se puede usar desde cualquier dispositivo con navegador 	&#128242;</h4>
                      <a href="https://kubodread.github.io/kubiotec/compostaje.html" target="_blank"> Visita la App Web </a>
                </article>
              </div>
</div>

<div class="contk1">
<TextoApp />   
</div>


  </div>

</template>

<script>
import TextoApp from './TextoApp.vue';




export default {
  name: 'HolaKubiotec',
  components: {
    TextoApp
  },
};
</script>

<style scoped>
h1 {
  color: #42b983;
}


.img1 {
  max-width: 40%;
}

  .inicioEntrada {
    display: flex;
    justify-content: center;
    padding:  15px 0;
    border-radius: 1em;
    margin: 5px;
  }

.contenedorK{
    display: flex;
    width: 90%; /* Asegura que el contenedor ocupe todo el ancho */
    height: auto;
    flex-wrap: nowrap;
    flex-direction: column;
    justify-content: center;
    margin: 5px 0 5px 0;
  overflow: auto;
}
.contk1 {
}

</style>