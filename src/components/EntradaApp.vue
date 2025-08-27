<template>
    <div :class="claseContenedor">
        <FichaEntrada 
            v-for="entrada in entradas"
            :key="entrada.id"
            :entrada="entrada"
        />
    </div>
</template>


<script>
import FichaEntrada from './FichaEntrada.vue'

import imgcw from './images/whatsp.png';
import imgcf from './images/faceboock.svg.webp';
import ajoloteImg from './images/ajolote.webp';
import lombrizAnzueloImg from './images/lombrizconanzuelo.webp';
import lombrizNucleoImg from './images/lombriznucleo.jpg';
import mmmicroImg from './images/mmmicro.webp';
import prodbalImg from './images/productosultrabal.jpg';


      
        const contactwN = "http://wa.me/+522281362858";


export default {
    name: 'EntradaApp',
    components: {
        FichaEntrada
    },
    data() {
        return {
        claseContenedor: 'claseContenedor',
        entradas: [
            { 
                id: 1,
                imagen: ajoloteImg,
                titulo: '¿Buscas un alimento rico y apetitoso?',
                subtitulo: ' La lombriz roja es un manjar nutritivo que tus mascotas adorarán.',
                descripcion: ' Desde <strong>ajolotes</strong>,<strong> peces </strong> hasta <strong> aves</strong>, <strong>reptiles y algunos roedores </strong>,                    un festín de proteínas y nutrientes esenciales en cada lombriz.                         </i> <span class="iconnoti">                        &#128031;  &#128019; &#129413; &#128013; &#129422; &#128001; &#129428;                        </span>                        <br> <br>                        ✨ ¡Potencia la salud de tus mascotas con lombriz roja californiana! ✨                        <br> <br>                        ¿Sabías que la lombriz roja es una fuente excepcional de proteína de alta calidad, <br>                        vitaminas y minerales esenciales para el bienestar de tus ajolotes, aves, reptiles y otras mascotas? 🦎🐦🐠 <br>',
                contactw: contactwN,
                mensajecon: 'Contacanos por whatsappn',
                contacF: 'https://www.facebook.com/share/19TVnGojng/',
                imgw: imgcw,
                imgf: imgcf
            }, 

             { 
                id: 2,
                imagen: lombrizAnzueloImg,
                titulo: 'Lombriz Roja para anzuelo',
                subtitulo: 'Venta de Lombriz roja viva para usar como anzuelo para pesca', descripcion: ' ¡Atrae la mejor pesca con el poder y sabor natural de la lombriz roja!<br>  Su color vibrante, su sabor irresistible para los peces y su movimiento natural en el agua  la convierten en el anzuelo perfecto para una jornada de pesca exitosa y ecológica. <br>   ¡Descubre la diferencia de forma sostenible en tu próxima aventura! <br>  Presentaciones de 20 - 50 - 100 lombrices',
                contactw: contactwN,
                mensajecon: 'Publicación vía Facebook',
                contacF: 'https://www.facebook.com/share/1Eq1LacWce/',
                imgw: imgcw,
                imgf: imgcf,
            },
             { 
                id: 3,
                imagen: lombrizNucleoImg,
                titulo: 'Venta de Lombriz Roja californiana',
                subtitulo: 'Inicia tu propia lombricomposta',
                descripcion: ' Venta de Lombriz roja californiana, la más eficiente para el proceso de compostaje, transforma del 60% al 80% de tus residuos en tierra rica en nutrientes. Te ayudamos a tener éxito en la transformación de los residuos orgánicos y contribuir a disminuir      la contaminación ambiental.     ',
                contactw: contactwN,
                mensajecon: 'Publicación Facebook',
                contacF: 'https://www.facebook.com/share/177cpKmr8Y/',
                imgw: imgcw,
                imgf: imgcf,
            },
             { 
                id: 4,
                imagen: mmmicroImg,
                titulo: 'Microorganismos benéficos',
                subtitulo: 'Te brindamos asesoramiento para que implementes el uso de microorganismos benéficos.',
                descripcion: '  Con el uso de las biotecnologías podemos acelerar el proceso de lombricompostaje y compostaje, disminuir malos olores y mejorar el producto final con microorganismos benéficos para las plantas.  <br> Descubre los beneficios de los microorganismos en tu plantas y cultivos, mejorando la salud del suelo y las plantas, aumentando la productividad de tus cultivos.',
                contactw: contactwN,
                mensajecon: 'Contactanos',
                contacF: contactwN,
                imgw: imgcw,
                imgf: imgcw,
            },
             { 
                id: 5,
                imagen: prodbalImg,
                titulo: 'Nutrientes agroecológicos para las plantas ',
                subtitulo: 'Distintos productos para todo tipo de plantas y cultivos',
                descripcion: 'Nutrientes a base de microorganismos benéficos, microorganismos benéficos, insecticidas y plaguicidas que no dañan tu salud ni contaminan el ambiente.<br>',
                contactw: contactwN,
                mensajecon: 'Conoce más sobre los productos',
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
.claseContenedor{
    display: flex;
    width: 90%; /* Asegura que el contenedor ocupe todo el ancho */
    height: auto;
    flex-wrap: wrap;
    justify-content: center;
    margin: 5px 0 5px 0;
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
    gap: 30px;           /* Añade espacio entre los productos */
  }
}
</style>