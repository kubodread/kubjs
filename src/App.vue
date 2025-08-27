<template>
  <div id="app">
    <ModalB v-if="mostrarModal" >
     <div>
      <h2>¡Bienvenido!</h2>
        <i>Como profesional en gestión ambiental, mi misión es promover el desarrollo sostenible.
        <br><br> A través de la aplicación de herramientas y estrategias especializadas, ofrezco soluciones que generan un impacto positivo en el entorno y la sociedad. 
         <br> <br> Mi trabajo se enfoca en:
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
         </i>
     </div>
    

             <button @click="ocultarModal">Aceptar</button>
    </ModalB>
    
     <div class="logoytext">
            <div class="logotextomovil">
                <a href="">
                  <img id="logo" src="../src/assets/logokubiotec.png" alt="Logo de Kubiotec">
                </a> 
                <a href="">
                  <p class="logotext">Kubiotec</p> 
                </a>
            </div>
      
            <div class="button-group">
            <button class="botonContenido" @click="cambiarContenido('HolaKubiotec')" >Inicio</button>
            <button class="botonContenido" @click="cambiarContenido('EntradaApp')"  >Lo más visto</button>
            <button class="botonContenido" @click="cambiarContenido('AsesoriaKub')"  >Información</button>
            <button class="botonContenido" @click="cambiarContenido('ProductoK')"  >Productos</button>
            <button ></button>
            </div>
            
      </div> <br>

<div class="content-display">
<transition name="fade" mode="out-in">
  <component :is="componenteActual"></component>
</transition>
</div>

    
  <HelloWorld msg="Welcome to Kubiotec"/>

</div>
  <br><br>
<footer>
     <div class="fologoytext">
            <div class="">
                  <p class="fologotext">Kubiotec 2025</p>  
            </div>
   
            
      </div></footer>

</template>

<script>
import HolaKubiotec from './components/HolaKubiotec.vue'
import ModalB from './components/ModalB.vue' // Importa el componente Modal
import BottonAcerca from './components/BottonAcerca.vue'
import EntradaApp from './components/EntradaApp.vue'
import AsesoriaKub from './components/AsesoriaKub.vue'
import ProductoK from './components/ProductoK.vue'

export default {
  name: 'App',
  components: {
    HolaKubiotec,
    ModalB,
    BottonAcerca,
    EntradaApp,
    AsesoriaKub,
    ProductoK
  },
   data() {
    return {
    componenteActual: 'HolaKubiotec',
      mostrarModal: true
    }
  },
  methods: {
    ocultarModal() {
      this.mostrarModal = false
    },
    cambiarContenido(componente) {
    this.componenteActual = componente;
    },
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
  margin-top: 10px;
}



/* Estilos para el modal */
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
  box-shadow: 0 5px 15px rgba(0,0,0,0.3);
}
button {
  margin: 10px;
  padding: 10px 20px;
  cursor: pointer;
}
/* Estilos para el modal */
/*estilo de entrada*/
    .logotextomovil {
        display: flex;
        flex-direction: row;
        align-items: center;
    }
        .logoytext {
        background-color: #1F2937;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        border-radius: 10px;

    }
      #logo {
        display: flex;
        align-content:flex-start;
        justify-content: flex-start;
        width: auto;
        height: 80px;
        flex-wrap: wrap;
        align-items: center;
        flex-direction: row;
    }   

   .logotextomovil a, .logotext {
        display: flex;
        align-content: center;
        justify-content: center;
        font-size: 48px;
        color:rgb(255, 255, 255);
    }
  button.logotextomovil  {
  cursor: pointer;
  border-radius: 5px;
  padding: 0 5px 0 5px;
  }

/* estilo para contenido*/
.container {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.button-group {
  margin-bottom: 20px;
}

.button-group button {
  padding: 10px 20px;
  margin: 5px 5px;
  font-size: 16px;
  cursor: pointer;
  background-color:rgb(43, 95, 0);
  color: white;
  border: none;
  border-radius: 5px;
}

.content-display {
  border: 1px solid #ddd;
  padding: 20px;
  border-radius: 8px;
  min-height: 200px; /* Evita que el contenedor se colapse */
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Transiciones para que el cambio entre componentes sea suave */
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s ease;
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
}

        .fologoytext {
        background-color: #1F2937;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        border-radius: 10px;
        text-size: 15px;
        color: #000000;
        
    }
      .fologoytext:hover { 
      color: #ffffff;
      box-shadow: inset 0 0 20px rgba(49, 138, 172, 0.5), 0 0 20px rgba(49, 138, 172, 0.4);
      outline-color: rgba(49, 138, 172, 0);
      outline-offset: 80px;
      text-shadow: 1px 1px 6px #fff;
      }
      .botonContenido:hover {
      color: #ffffff;
      box-shadow: inset 0 0 20px rgba(49, 138, 172, 0.5), 0 0 20px rgba(49, 138, 172, 0.4);
      outline-color: rgba(49, 138, 172, 0);
      outline-offset: 80px;
      text-shadow: 1px 1px 6px #fff;
      }
</style>
