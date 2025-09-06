<template>
  <div id="app">
    <ModalB v-if="mostrarModal" >
     <div>
      <h2>¡Bienvenido!</h2>
        <i>Como profesional en gestión ambiental, mi misión es promover el desarrollo sostenible.
        <br><br>
          <div class="imgl">
          <img id="logo" src="../src/components/images/ciudadv.svg" alt="ciudad sostenible">
          <img id="logo" src="../src/components/images/arbolv.svg" alt="arbol sostenibilidad">
        </div>
        <br> A través de la aplicación de herramientas y estrategias especializadas, ofrezco soluciones que generan un impacto positivo en el entorno y la sociedad. 
        <br><br>
        <div class="imgl">
          <img id="logo" src="../src/components/images/luz.svg" alt="ciudad sostenible">
          <img id="logo" src="../src/components/images/rec.svg" alt="arbol sostenibilidad">
          <img id="logo" src="../src/components/images/mundo.svg" alt="arbol sostenibilidad">
        </div>

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
            </div>
      
<div>
    <button class="hamburger-menu" @click="toggleMenu">
      <span></span>
      <span></span>
      <span></span>
    </button>
    
    <div :class="['button-group', { 'is-open': isMenuOpen }]">
      <ul class="button-group-list">
        <li>
          <button class="botonContenido" @click="cambiarContenido('HolaKubiotec')">Inicio</button>
        </li>
        <li>
          <button class="botonContenido" @click="cambiarContenido('EntradaApp')">Lo más visto</button>
        </li>
        <li>
          <button class="botonContenido" @click="cambiarContenido('AsesoriaKub')">Información</button>
        </li>
        <li class="has-submenu">
          <button class="botonContenido" @click="toggleAppsSubmenu">Apps</button>
          
          <ul class="submenu" v-if="isAppsSubmenuOpen">
            <li>
              <button class="botonContenido" @click="cambiarContenido('ControlComposta')">Composta-Control</button>
            </li>
            <li>
              <button class="botonContenido" @click="cambiarContenido('Control2')">Apps2</button>
            </li>
            <li>
              <button class="botonContenido" @click="cambiarContenido('Control3')">Apps3</button>
            </li>
          </ul>
        </li>
        <li>
          <button class="botonContenido" @click="cambiarContenido('ProductoK')">Productos</button>
        </li>

      </ul>
    </div>
  </div>
            
      </div> <br>

 <Loader v-if="isLoading" />

<div v-show="!isLoading" class="content-display">
<transition name="fade" mode="out-in">
  <component :is="componenteActual"></component>
</transition>
</div>

    

</div>
  <br><br>
<footer>
     <div class="fologoytext">
            <div class="fologotext">
                  <p class="fologotext">⚡ by <a href="mailto:kubiotecmx@gmail.com" target="_blank"> Kubiotec</a> 📲</p>  
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
import ControlComposta from './components/ControlComposta.vue'
import { ref, watch } from 'vue';
import Loader from './components/Loader.vue';


export default {
  name: 'App',
  components: {
    HolaKubiotec,
    ModalB,
    BottonAcerca,
    EntradaApp,
    AsesoriaKub,
    ProductoK,
    ControlComposta,
    Loader
  },
     setup() {
    // Variables reactivas para el estado
    const isLoading = ref(false);
    const componenteActual = ref(HolaKubiotec);
    const mostrarModal = ref(true);
    const isAppsSubmenuOpen = ref(false)


    const ocultarModal = () => {
      mostrarModal.value = false;
    };


    const isMenuOpen = ref(false);
    const toggleMenu = () => {
      isMenuOpen.value =!isMenuOpen.value;
    };

    const toggleAppsSubmenu = () => {
      isAppsSubmenuOpen.value =!isAppsSubmenuOpen.value;
    };


    // Método para cambiar el componente y manejar el loader
    const cambiarContenido = (componente) => {
      // Muestra el loader inmediatamente
      isLoading.value = true;
      // Asigna el nuevo componente
      componenteActual.value = componente;
      
      // Simula el tiempo de carga
      setTimeout(() => {
        // Oculta el loader cuando la carga "termina"
        isLoading.value = false;
      }, 400);
      isMenuOpen.value = false;
      isAppsSubmenuOpen.value = false;

    };

    // Puedes usar watch aquí para observar componenteActual
    // si la lógica de carga fuera más compleja
    /*
    watch(componenteActual, (nuevoComponente) => {
      if (nuevoComponente) {
        isLoading.value = true;
        setTimeout(() => {
          isLoading.value = false;
        }, 100);
      }
    });
    */

    // Devuelve el estado y los métodos para que la plantilla pueda usarlos
    return {
      isLoading,
      componenteActual,
      cambiarContenido,
      mostrarModal,
      ocultarModal,
      isMenuOpen,
      toggleMenu,
      isAppsSubmenuOpen,
      toggleAppsSubmenu,
    };
  },
  }


</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 10px; */
}

body {
  margin: 0;
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

ul {
  list-style: none;
}
.imgl{
  display: flex;
  flex-direction: row;
  justify-content: center;
}
button {
  margin: 0 10px;
  padding: 5px 10px;
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
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
      position: sticky;
      top: 0;
      z-index: 10;
    }

      #logo {
        display: flex;
        align-content:flex-start;
        justify-content: flex-start;
        width: auto;
        height: 40px;
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
  margin: 0 5px;
  display: flex;
}

.button-group button {
  padding: 5px 5px;
  margin: 0 5px;
  font-size: 16px;
  cursor: pointer;
  background-color:rgb(43, 95, 0);
  color: white;
  border: none;
  border-radius: 5px;
}

.content-display {
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

        div.fologoytext {
        background-color: #00000079;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        font-size: 15px;
        color:rgb(0, 0, 0);
        width: fit-content;
        padding: 0 0;
        position: fixed;
        bottom: 0;
    }
      .fologoytext:hover { 
      color: #ffffff;
      box-shadow: inset 0 0 20px rgb(255, 250, 178), 0 0 10px rgb(255, 235, 144);
      /*outline-color: rgb(49, 137, 172);
      outline-offset: 80px;
      text-shadow: 1px 1px 4px #fff;*/
      }

      a {
        color: blue;
      }

      p.fologotext , a{
        color: black;
        font-weight: 600;
        width: fit-content;
        padding:  5px;
        margin: 0;
      }
      .botonContenido:hover {
      color: #ffffff;
      box-shadow: inset 0 0 20px rgba(49, 138, 172, 0.5), 0 0 20px rgba(49, 138, 172, 0.4);
      outline-color: rgba(49, 138, 172, 0);
      outline-offset: 80px;
      text-shadow: 1px 1px 6px #fff;
      }

      /* Estilos para pantallas grandes (desktop) */
.hamburger-menu {
  display: none; /* Oculta el botón de hamburguesa en desktop */
}

.button-group-list {
  display: flex; /* Muestra los botones en fila */
  list-style: none;
  padding: 0;
  margin: 0;
}

.button-group-list li {
  margin: 0 10px;
}

/* Estilos para el elemento de la lista que contiene el submenú */
.button-group-list .has-submenu {
  position: relative; /* Es importante para que el submenú se posicione en relación a este elemento */
}

/* Estilos para el submenú */
.submenu {
  position: absolute;
  top: 100%; /* Posiciona el submenú justo debajo del botón padre */
  left: 0;
  background-color:rgb(43, 95, 0);
  list-style: none;
  padding: 10px;
  border-radius: 4px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
  z-index: 10;
}

/* Opcional: Estilos para los botones dentro del submenú */
.submenu .botonContenido {
  width: fit-content;
  text-align: center;
  /* Otros estilos que necesites */
}


/* Estilos para pantallas pequeñas (móviles) */
@media (max-width: 768px) {
  .hamburger-menu {
    display: block; /* Muestra el botón de hamburguesa */
    background: none;
    border: none;
    cursor: pointer;
    z-index: 100;
  }
  
  .hamburger-menu span {
    display: block;
    width: 25px;
    height: 3px;
    background-color: #333;
    margin: 5px 0;
  }
  
  .button-group {
    display: none; /* Oculta el menú por defecto */
    flex-direction: column;
    position: absolute;
    top: 60px; /* Ajusta esto a la altura de tu barra de navegación */
    left: 0;
    width: 100%;
    background-color: #fff;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    z-index: 99;
  }
  
  .button-group.is-open {
    display: flex; /* Muestra el menú cuando tiene la clase 'is-open' */
      background-color:rgb(43, 95, 0);
      width: fit-content;

  }
  
  .button-group-list {
    flex-direction: column;
    width: fit-content;
  }
  
  .button-group-list li {
    width: fit-content%;
    text-align: center;
    border-bottom: 1px solid #eee;
  }
  /* Estilos para el elemento de la lista que contiene el submenú */
.button-group-list .has-submenu {
  position: relative; /* Es importante para que el submenú se posicione en relación a este elemento */
}

/* Estilos para el submenú */
.submenu {
  position: relative;
  top: 100%; /* Posiciona el submenú justo debajo del botón padre */
  left: 0;
  background-color:rgb(43, 95, 0);
  list-style: none;
  padding: 10px;
  border-radius: 4px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
  min-width: 150px; /* Ancho mínimo para que los botones se vean bien */
  z-index: 10;
}

/* Opcional: Estilos para los botones dentro del submenú */
.submenu .botonContenido {
  width: 100%;
  text-align: center;
  /* Otros estilos que necesites */
}
}


</style>
