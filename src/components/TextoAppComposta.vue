<template>
    <div :class="claseContenedor">
        <ImgText 
            v-for="texto in textos"
            :key="texto.id"
            :texto="texto"
        />
    </div>
</template>


<script>
import ImgText from './ImgText.vue';

import img1 from './images/ .jpeg';
import img2 from './images/ .jpeg';
import img3 from './images/.jpeg';
import img4 from './images/.jpeg';


export default {
    name: 'TextoAppComposta',
    components:{
        ImgText
    },
    data() {
        return {
                claseContenedor: 'claseContenedor',

            textos: [
            { 
                id: 1,
                imagen: separa,
                informacion: 'Separar los residuos ayuda a disminuir los malos olores, a mitigar la problemática de la contaminación y facilitar el reciclaje de materiales inorgánicos principalmente plásticos',
            },
            { 
                id: 2,
                imagen: manosT ,
                informacion: 'Al gestionar los residuos orgánicos podemos transformarlos en tierra, por medio del compostaje, una practica sustentable para el ambiente',
            },
            { 
                id: 3,
                imagen: jardinr,
                informacion: 'La salud de las plantas esta relacionada con una buena nutrición y diversidad de microorganismos benéficos en el suelo',
            },
            { 
                id: 4,
                imagen: jardind,
                informacion: 'La propuesta: desarrollarnos de la mano con el ambiente, el uso de las bio tecnologías es fundamental para un desarrollo sustentable ',
            },
            ],   
        }
    }
};

</script>


<style scoped>
.claseContenedor {
        display: flex;
        flex-direction: column;
        border: 3px;
        border-color: #3882f6;
        padding-top: 5px;
        justify-content: space-between;
        gap: 3px;
        align-items: start;
        flex-wrap: wrap;
        align-content: center;
    }


/* Media Query para pantallas de escritorio.
  Cuando la pantalla tiene un ancho mínimo de 768px (o más),
  se aplican estos estilos.
*/
@media (min-width: 768px) {
  .claseContenedor {
    flex-direction: row; /* Vuelven a ser filas */
    flex-wrap: wrap;     /* Permite que los productos pasen a la siguiente fila */
    justify-content: center;
    max-width: 1200px;   /* Reduce el ancho máximo del contenedor */
    margin: 0 auto;      /* Centra el contenedor en la pantalla */
    gap: 10px;           /* Añade espacio entre los productos */
  }
  }
</style>