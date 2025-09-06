<template>
  <div  class=""> 

  <div :class="claseContenedor">
        <FichaEntrada 
            v-for="entrada in entradas"
            :key="entrada.id"
            :entrada="entrada"
        />
  </div>
  </div>
</template>

<script>
import FichaEntrada from './FichaEntrada.vue'


import imgcw from './images/whatsp.png';
import proyectosImg from './images/proyectos.webp';

const contactwN = "http://wa.me/+522281362858";


export default {
  name: 'AsesoriaKub',
  components: {
    FichaEntrada
  },
  data() {
    return {
    claseContenedor: 'claseContenedor',
    entradas: [
      {
                 id: 1,
                imagen: proyectosImg,
                titulo: 'Transformando Ideas en Impacto Sostenible ',
                subtitulo: 'Importancia del Enfoque Biológico en la Asesoría',
                descripcion: 'Como Biólogo y Especialista en Gestión Ambiental, ofrezco soluciones integrales para el desarrollo sostenible. <br> <br> Mi enfoque combina el conocimiento técnico y científico con una sólida experiencia en la gestión de proyectos y la capacitación comunitaria. <br><br> Mi objetivo es convertir sus ideas en proyectos viables que generen un impacto positivo en el entorno y la sociedad. <br> <h2> Servicios Destacados </h2> <strong> <i> Optimización y Gestión de Procesos:</i> </strong> Implemento soluciones tecnológicas y programas de capacitación de personal para agilizar procesos administrativos, sociales y logísticos. Mi enfoque abarca desde la recopilación de datos clave hasta la aplicación de herramientas en entornos técnicos y comunitarios, generando beneficios económicos, sociales y ambientales. <br><br> <strong><i> Proyectos de Sostenibilidad: </i></strong> Diseño y ejecución de iniciativas de gestión de residuos orgánicos, sistemas de captación de agua pluvial y programas de reforestación con especies nativas. <br><br> <strong><i> Asesoramiento y Cumplimiento Normativo: </i></strong> Brindo asesoramiento experto para el cumplimiento legal y ambiental, elaborando memorias técnicas y documentación necesaria para trámites y permisos.<br><br> <strong> <i> Capacitación y Educación: </i> </strong> Lidero talleres participativos y campañas de educación ambiental, promoviendo una cultura de concientización sobre agroecología, salud y bienestar. <br><br> <strong> <i> Paisajismo y Diseño Funcional: </i> </strong> <br> Creación de proyectos de paisajismo y diseño de viveros, combinando la funcionalidad con la estética para un impacto visual y productivo.<br> <br>',
                contactw: contactwN,
                mensajecon: 'Contactanos por whatsappn',
                contacF: contactwN,
                imgw: imgcw,
                imgf: imgcw,       
      },
    ],
    };
  }
  
};
</script>

<style scoped>
h1 {
  color: #42b983;
}
button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
  background-color: #35495e;
  color: white;
  border: none;
  border-radius: 5px;
}

.img1 {
  max-width: 40%;
}


.contenedorK{
    display: flex;
    width: 90%; /* Asegura que el contenedor ocupe todo el ancho */
    height: auto;
    flex-wrap: wrap;
    flex-direction: column;
    justify-content: center;
    margin: 5px 0 5px 0;
}

@media (min-width: 768px) {
  .claseContenedor {
 flex-direction: row; /* Vuelven a ser filas */
  display: flex;
    flex-wrap: wrap;     /* Permite que los productos pasen a la siguiente fila */
    justify-content: center;
    max-width: 1200px;   /* Reduce el ancho máximo del contenedor */
    margin: 0 auto;      /* Centra el contenedor en la pantalla */
    gap: 30px;           /* Añade espacio entre los productos */
  }

  .inicioEntrada {
    width: 60%; 
    max-width: 350px; /* Evita que crezca demasiado */
    display: flex; 
    justify-content:center;
    border: 0;
  }


  .inicioEntrada{
    max-width: 100%;
  }

  .contenedorK{
    display: flex;
    width: 90%; /* Asegura que el contenedor ocupe todo el ancho */
    height: auto;
    flex-wrap: wrap;
    flex-direction: column;
    justify-content: center;
    margin: 5px 0 5px 0;
}
  .textfproductoslombcar{
    justify-content: center;
  }

  }
</style>