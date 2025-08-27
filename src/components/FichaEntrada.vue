<template>
   <div class="inicioEntrada">
    
    <div class="figtproductos">
        <img class="lombriprocarrusel" :src="entrada.imagen" :alt="entrada.titulo">

        <div class="textfproductoslombcar">
       
            <h1 class="tituEntrada">{{ entrada.titulo }}</h1> 
            <article>
            <h2><strong> {{ entrada.subtitulo }} </strong></h2>
            
            <div v-html="entrada.descripcion"></div>
             
               </article>
      
            <div class="nivelcontacto">
                <div class="contactw">
                <button class="contactw "><a class="conTac" :href='entrada.contactw'>
                    {{ entrada.mensajecon }}
                </a></button> 
                </div>  
                <div class="contactw">
                <a class="conTac" :href='entrada.contacF' target="_blank"> 
                    <img id="insta" :src="entrada.imgf" alt="Contacto" />
                </a> <br>   
                </div>
                <div class="contactw">
                <a class="conTac" :href='entrada.contactw' target="_blank"> <img id="insta" :src="entrada.imgw" alt="Contacto" /></a> <br>   
                </div>
            </div>
        </div>
    </div>
  </div>
</template>


<script>
export default {
    name: 'FichaEntrada',
    props: { 
        entrada: {
            type: Object,
            required: true,
        },
    },
};


</script>

<style scoped>


.texto1{
    text-align: center;
}

  .inicioEntrada {
  border: 1px solid #ccc;
  padding: 35px;
  margin: 10px;
  border-radius: 8px;
  text-align: center;
  display: flex;
  justify-content: center;
  }

.tituEntrada {
display: flex;
    justify-content: center;
    text-align: center;
}

.figtproductos {
  max-width: 90%; /* Tamaño del contenedor */
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.lombriprocarrusel{
    max-width: 80%;
    height: auto;
    border-radius: 10px;
    display: flex;
    object-fit: contain;
    justify-content: center;
}
.textfproductoslombcar {
    background-color: rgba(211, 211, 211, 0.432);
    text-align: justify;
    font-size: 15px;
    width: auto;
    height: auto;
    padding-top:3px;
    padding-right: 25px;
    padding-left: 25px;
    border-radius: 15px;
    margin: 5px 0 10px 0;
}

    #whatsappn {
        width: auto;
        height: 25px;
    }

    #insta {
        width: auto;
        height: 45px;
    }
    .conTac {
        color: #000000; 
    }
    .contactw {
        display: flex;
        align-content: center;
        align-items: center;
        color: #0000 !important;
        font-size: 20px;
        font-weight: 500;
        border-radius: 0.5em 1.2em;
        background: #318aac;
        position: relative;
        border: 2px solid #318aac;
        outline: 2px solid;
        outline-color: rgba(49, 138, 172, 0.4);
        transition: all 1s cubic-bezier(0.19, 1, 0.22, 1);
       }
    
       .contactw:hover{
        box-shadow: inset 0 0 20px rgba(49, 138, 172, 0.5), 0 0 20px rgba(49, 138, 172, 0.4);
        outline-color: rgba(49, 138, 172, 0);
        outline-offset: 80px;
        text-shadow: 1px 1px 6px #fff;
        }

.nivelcontacto {
    display: flex;
    flex-direction: row;
}
    article {
        padding: 2%;
        display: flex;
        flex-direction: column;
        text-align: justify;
        }
/* Media Query para escritorio */
@media (min-width: 768px) {
  .inicioEntrada {
    /* Calcula el ancho para que quepan 2 o 3 fichas en una fila.
      calc() es muy útil para esto.
    */
    width: calc(33.33% - 20px); /* 33.33% - el espacio de gap */
    max-width: 350px; /* Evita que crezca demasiado */
    display: flex; 
    justify-content:center;
  }

  .tituEntrada {
display: flex;
    justify-content: center;
    text-align: center;
}

.figtproductos {
  max-width: 90%; /* Tamaño del contenedor */
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.lombriprocarrusel{
    max-width: 80%;
    height: auto;
    border-radius: 10px;
    display: flex;
    object-fit: contain;
    justify-content: center;
}
.textfproductoslombcar {
    display: flex;
    flex-wrap: wrap;
    background-color: rgba(211, 211, 211, 0.432);
    text-align: justify;
    font-size: 15px;
    width: auto;
    height: auto;

    border-radius: 15px;
    margin: 5px 0 10px 0;
}

    #whatsappn {
        width: auto;
        height: 25px;
    }

    #insta {
        width: auto;
        height: 45px;
    }
    .conTac {
        color: #000000; 
    }
    .contactw {
        display: flex;
        align-content: center;
        align-items: center;
        color: #0000 !important;
        font-size: 20px;
        font-weight: 500;
        border-radius: 0.5em 1.2em;
        background: #318aac;
        position: relative;
        border: 2px solid #318aac;
        outline: 2px solid;
        outline-color: rgba(49, 138, 172, 0.4);
        transition: all 1s cubic-bezier(0.19, 1, 0.22, 1);
       }
    
       .contactw:hover{
        box-shadow: inset 0 0 20px rgba(49, 138, 172, 0.5), 0 0 20px rgba(49, 138, 172, 0.4);
        outline-color: rgba(49, 138, 172, 0);
        outline-offset: 80px;
        text-shadow: 1px 1px 6px #fff;
        }

.nivelcontacto {
    display: flex;
    flex-direction: row;
}
    article {
        padding: 2%;
        display: flex;
        flex-direction: column;
        text-align: justify;
        }
}
</style>