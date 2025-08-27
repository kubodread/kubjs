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
import FichaEntrada from './FichaEntrada.vue';

export default {
    name: 'EntradaApp',
    components: {
        FichaEntrada
    }
    data() {
        return {
            entradas: [
            { 
                id: 1,
                imagen: '',
                titulo: '',
                subtitulo: '',
                descripcion: '',
                contactw: '',
                mensajecon: '',
                contacF: '',
                imgw: '',
                imgf: '',
            }, 
            { 
                id: 2,
                imagen: '',
                titulo: '',
                subtitulo: '',
                descripcion: '',
                contactw: '',
                mensajecon: '',
                contacF: '',
                imgw: '',
                imgf: '',
            },
             { 
                id: 3,
                imagen: '',
                titulo: '',
                subtitulo: '',
                descripcion: '',
                contactw: '',
                mensajecon: '',
                contacF: '',
                imgw: '',
                imgf: '',
            },
             { 
                id: 4,
                imagen: '',
                titulo: '',
                subtitulo: '',
                descripcion: '',
                contactw: '',
                mensajecon: '',
                contacF: '',
                imgw: '',
                imgf: '',
            },
             { 
                id: 5,
                imagen: '',
                titulo: '',
                subtitulo: '',
                descripcion: '',
                contactw: '',
                mensajecon: '',
                contacF: '',
                imgw: '',
                imgf: '',
            },
             { 
                id: 6,
                imagen: '',
                titulo: '',
                subtitulo: '',
                descripcion: '',
                contactw: '',
                mensajecon: '',
                contacF: '',
                imgw: '',
                imgf: '',
            },

            ]
        {
    }
}
</script>


<style scoped>
.claseContenedor{
    display: flex;
    flex-wrap: wrap;
    justify-content:center;
}
</style>