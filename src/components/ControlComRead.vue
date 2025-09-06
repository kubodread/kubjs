
<template>
<div class="articuloK">
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

    
    <div class="articuloK">
        <h1>
Composta-Control
</h1> 
<h2>
 Controlador de Composta por Kubiotec    
   
</h2>

<h3>
 **Controlador de Composta** es una aplicación web progresiva (PWA) diseñada para ayudarte a gestionar, monitorear y optimizar tus pilas de compostaje de manera eficiente. La aplicación funciona sin conexión a internet una vez que se ha cargado por primera vez, permitiéndote registrar datos en cualquier lugar.
   
</h3>
<p>
 visita en <a href="http://composta-control.vercel.app/" target="_blank"> https://composta-control.vercel.app/</a>  
</p>

<h3>
  Características Principales  
</h3>
    </div>


<div class="articuloK">
    <ul>
        <il>
           <p>
             <h4>
                Gestión Integral de Perfiles de Compostaje
             </h4>
             <p>
                - **Múltiples Perfiles:** Crea y gestiona perfiles para cada una de tus pilas de composta de forma independiente.
- **Personalización:** Asigna un nombre y un color distintivo a cada perfil para una fácil identificación visual en los gráficos.
- **Persistencia Local:** Todos tus datos se almacenan de forma segura en el `localStorage` de tu navegador, lo que garantiza privacidad y funcionalidad offline.
            </p>
            <p>
                <h4>
                     Balance de Relación Carbono:Nitrógeno (C:N)
                </h4>
                <p>
                    Una relación C:N adecuada es crucial para un compostaje eficiente. La aplicación te ayuda a:
                    - **Calcular la Relación C:N:** Añade materiales ricos en carbono (marrones) y nitrógeno (verdes) de una lista predefinida.
                    - **Especificar Cantidades:** Define la cantidad (en "partes" relativas) de cada material que has añadido a tu pila.
                    - **Obtener una Estimación:** La aplicación calcula una relación C:N estimada para tu mezcla, ayudándote a ajustarla para alcanzar el rango ideal (típicamente entre 25:1 y 30:1).
                    - **Guardar y Anotar:** Guarda la composición de tu mezcla y añade notas o recomendaciones para futuros ajustes.
                </p>
            </p>
            <p>
                <h4>
                    Monitoreo y Registro de Datos Detallado
                </h4>
                <p>
                    Registra parámetros clave de tu pila de composta para un seguimiento preciso:
                    - **Temperatura de la Composta (°C)**
                    - **Humedad (%)**
                    - **pH** (Opcional)
                    - **Conductividad Eléctrica (CE) en dS/m** (Opcional)
                    - **Temperatura Ambiental (°C)** (Opcional)
                    - **Notas y Observaciones**
                </p>
            </p>

          </p>
        </il>
        <il>
            <p>
                <h4>
                    Visualización con Gráficos Interactivos
                </h4>
                <p>
Analiza el progreso de tu compostaje a lo largo del tiempo con gráficos fáciles de entender:
- **Gráfico de Temperaturas:** Compara la temperatura interna de la composta con la temperatura ambiental.
- **Gráfico de Humedad:** Monitorea la evolución de la humedad.
- **Gráficos de pH y CE:** Visualiza las tendencias de estos parámetros si decides registrarlos.
                </p>
            </p>


        </il>
        <il>

        </il>
        <il>
            <p>
             <h4>
                 Importar y Exportar Datos (CSV)
            </h4>
                <p>
                    <p>
                        Puedes fácilmente respaldar tus datos o importarlos desde otras fuentes usando archivos CSV.

                    </p>

                    <p>
                        <h4>
                         Exportar Datos

                        </h4>
                            La aplicación te permite descargar todos los registros de un perfil en un archivo CSV con un solo clic.
                    </p>
                    <p>
                        <h4>

                     Importar Datos
                        </h4>
                        <p>
                        Para importar datos a un perfil, tu archivo CSV debe tener una estructura específica.
                    
                        </p>
                    </p>
                    <p>
                        <h4>
                    Columnas Requeridas
                        </h4>
                    <p>
                        Las siguientes columnas son **obligatorias**:
                        - `Date` o `Fecha`
                        - `Temperature_C` o `Temperatura (°C)`
                        - `Humidity_pc` o `Humedad (%)`
                    </p>
                    </p>

                    <p>
                        <h4>
                            Columnas Opcionales
                        </h4>
                        <p>
                            Puedes incluir estas columnas si tienes los datos:
                    - `pH`
                    - `EC_dS_m` o `CE (dS/m)`
                    - `AmbientTemperature_C` o `Temperatura_Ambiental_C`
                    - `Notes` o `Notas`
                        </p>
                    </p>
                    <p>
                        <h4>
                    **Nota:** La aplicación es flexible con los nombres de las columnas y reconoce las variaciones comunes mencionadas anteriormente (insensible a mayúsculas/minúsculas).

                        </h4>
                        <p>


                    Formato de Fecha
                    El importador es inteligente y puede detectar automáticamente una variedad de formatos de fecha. Para asegurar la máxima compatibilidad, se recomienda usar el formato **ISO 8601**. Sin embargo, también se suelen reconocer los siguientes formatos:
                    - `YYYY-MM-DD HH:mm:ss` (ej: `2023-10-27 14:30:00`)
                    - `YYYY-MM-DD` (ej: `2023-10-27`)
                    - `DD/MM/YYYY` (ej: `27/10/2023`)
                    - `MM/DD/YYYY` (ej: `10/27/2023`)

                    El importador analizará las primeras filas para deducir el formato correcto y lo aplicará al resto del archivo.

                     Ejemplo de Archivo CSV Válido:
                    ```csv
                    Date, Temperature_C, Humidity_pc ,pH ,EC_dS_m ,Notes
                    2023-10-27 15:00:00,55.5,62.1,6.8,2.1,"Se realizó el primer volteo"
                    2023-10-28 16:00:00,58.2,60.5,,,
                    2023-10-29 14:30:00,60.1,59.8,6.7,2.3,"Se añadió un poco de agua"
                    ```

                        </p>
                    </p>



---

                </p>
            </p>
        </il>
        <il>
            <p>
                <h4>
                    Pila Tecnológica
                </h4>
                <p>
                    - **Framework:** Next.js (con App Router)
                    - **Lenguaje:** TypeScript
                    - **UI:** React, ShadCN UI, Tailwind CSS
                    - **Gráficos:** Recharts
                    - **Funcionalidad Offline:** Progressive Web App (PWA) con Service Workers.
                    - **Almacenamiento:** LocalStorage del navegador.
                </p>
            </p>            
        </il>
    </ul>
</div> 
</div>


</template>

<script>
export default {
    name: 'ControlComRead',
    props: {
        claseContenedor: {
        type: String,
        required: true
        
    }
}
};
</script>

<style scoped>

  .inicioEntrada {
    display: flex;
    justify-content: center;
    align-content: center;
    padding:  0px 0;
    border-radius: 1em;
    margin: 5px;
  }
.contk1 {
    text-align: center;
    border-bottom: solid 1px;
}
.articuloK {
    width: 90%;
    padding: 0 5px;
    min-width: 250px;
    max-width: 1000px;
}

</style>