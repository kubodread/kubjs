<template>
  <div class="productos-container">
    <FichaProducto 
      v-for="producto in productos"
      :key="producto.id"
      :producto="producto"
    />
  </div>
</template>

<script>
import FichaProducto from './FichaProducto.vue'; // Importa el nuevo componente

import ajolote from './images/ajolote.webp';
import balblogosolo  from './images/balblogosolo.jpg';
import ultraballogo from './images/ultraballogo.png';
import sulfocaldologo from './images/sulfocaldologo.png';
import alfinjabonlogo  from './images/alfinjabonlogo.jpg';
import alfinmultiminerallogo from './images/alfinmultiminerallogo.png';
import tdlogo  from './images/tdlogo.png';
import mmasolidoslogosolo  from './images/mmasolidoslogosolo.jpg';


export default {
  name: 'ProductoK',
  components: {
    FichaProducto
  },
  data() {
    return {
      productos: [
        {
        id: 1,
        imagen: ajolote,
        titulo: '¿Buscas un alimento rico y apetitoso?',
        descripcion: 'La lombriz roja es un manjar nutritivo que tus mascotas adorarán. ¿Quieres ver a tus mascotas más activas y saludables? 💪 La lombriz roja californiana fortalece su sistema inmunológico y mejora su piel/pelaje/plumaje. ¡Un bocado nutritivo que aman! Presentaciones de 20, 50 y 100 lombrices.',
        informacionCompleta: ''
      },
      {
        id: 2,
        imagen: balblogosolo,
        titulo: 'Bacterias ácido lácticas: microorganismos benéficos',
        descripcion: 'Bacterias Benéficas para el combate del estrés hídrico y prevención de enfermedades. Ademas promueve y estimula a las plantas para la floración. El empleo estratégico de microorganismos benéficos para la remediación ambiental en entornos agrícolas y urbanos es crucial. La aplicación de microorganismos específicos para la restauración de suelos degradados, la descontaminación de aguas residuales y la gestión de residuos representa un enfoque prometedor para abordar problemáticas ambientales presentes en estos entornos.',
        informacionCompleta: ''
      },
      {
        id: 3,
        imagen: ultraballogo,
        titulo: 'Ultrabal: alto en nutrientes',
        descripcion: 'Bacterias Benéficas con alta cantidad de nutrientes para el desarrollo de las plantas, ideal para el crecimiento y la floración.',
        informacionCompleta: ''
      },
      {
        id: 4,
        imagen: sulfocaldologo,
        titulo: 'SulfoCaldo: para control de plagas',
        descripcion: 'El Caldo Sulfocálcico, una mezcla con Sulfuro de Calcio como ingrediente activo, es un aliado potente en la agricultura, reconocido por sus beneficios múltiples en la prevención y el control de enfermedades, así como en el aporte nutrimental a las plantas.',
        informacionCompleta: ''
      },
      {
        id: 5,
        imagen: alfinjabonlogo,
        titulo: 'Al-fin Jabón: para controlar plagas Aliado para el combate de plagas en nuestras plantas.',
        descripcion: 'El jabón potásico es un producto natural derivado de la reacción de potasa cáustica con ácidos grasos vegetales. Se utiliza ampliamente en agricultura orgánica debido a su bajo impacto ambiental y su eficacia en el control de plagas. Es importante resaltar que no deja residuos tóxicos y es amigable con los organismos beneficiosos del suelo.',
        informacionCompleta: ''
      },
      {
        id: 6,
        imagen: alfinmultiminerallogo,
        titulo: 'Al-Fin Multimineral: Aliadas para plantas fuertes y sanas',
        descripcion: 'Mezcla de leonarditas y zeolitas, aportan nutrientes esenciales para las plantas: La leonardita es rica en ácidos húmicos y fúlvicos, que mejoran la absorción de nutrientes y estimulan el crecimiento de las plantas. La zeolita, por su parte, aporta macro y micronutrientes esenciales para el desarrollo óptimo de las plantas.',
        informacionCompleta: ''
      },
      {
        id: 7,
        imagen: tdlogo,
        titulo: 'TD Tierra de Diatomeas: Contra insectos, hormigas, chinches y cucarachas',
        descripcion: 'La tierra de diatomeas es un polvo fino de origen natural compuesto por restos fosilizados de algas microscópicas llamadas diatomeas. Es un producto versátil y ecológico que ofrece diversos beneficios: Control de plagas ✔️Salud de las plantas ✔️Fortalece las plantas ✔️Desodorante y absorbente ✔️Es importante destacar que la tierra de diatomeas es biodegradable, no tóxica para humanos, mascotas ni plantas, y segura para el medio ambiente.',
        informacionCompleta: ''
      },
      {
        id: 8,
        imagen: mmasolidoslogosolo,
        titulo: 'Microorganismos de Montaña sólidos (MMA): Explorando el Poder de la Naturaleza en la Agricultura',
        descripcion: 'Los Microorganismos de Montaña (MMA) constituyen una mezcla vital de bacterias, hongos, levaduras y otros microorganismos beneficiosos que encuentran su hogar y desarrollo en los entornos naturales de bosques y selvas. Su capacidad para incorporarse tanto al suelo como a los abonos orgánicos mejora la disponibilidad de nutrientes cruciales para el crecimiento de las plantas, brindando así un soporte vital en la optimización de la productividad agrícola.',
        informacionCompleta: ''
      }
      ]
    };
  }
};
</script>

<style scoped>
.productos-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

/* Media Query para pantallas de escritorio.
  Cuando la pantalla tiene un ancho mínimo de 768px (o más),
  se aplican estos estilos.
*/
@media (min-width: 768px) {
  .productos-container {
    flex-direction: row; /* Vuelven a ser filas */
    flex-wrap: wrap;     /* Permite que los productos pasen a la siguiente fila */
    justify-content: center;
    max-width: 1200px;   /* Reduce el ancho máximo del contenedor */
    margin: 0 auto;      /* Centra el contenedor en la pantalla */
    gap: 20px;           /* Añade espacio entre los productos */
  }
}


</style>