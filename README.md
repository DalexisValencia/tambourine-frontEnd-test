<p align="center">
  <h1 align="center"><b>Cerveza Golden - Roulette</b></h1>
</p>

## Tabla de contenido

- [Comenzando](#comenzando-🚀)
- [Requerimientos del sistema](#requerimientos-del-sistema-📋)
- [Configuración](#configuración-🔧)
- [Como Ejecutar](#como-ejecutar-🕹️)
- [Imagenes](#imagenes-🕹️)
- [Colaboradores](#colaboradores-🏓)


## Comenzando 🚀

Este manual permitira continuar manejando el flujo de desarrollo en el mantenimiento de este proyecto, tanto en el procesamiento de los estilos como en el manejo optimo de las imagenes.

> ⚠️ **Por favor NO sobreescribir estilos con hojas externas**, al inspeccionar los elementos se puede evidenciar la seccion correspondiente a modificar gracias al archivo *.map* que acompaña cada hoja de estilos.


## Requerimientos del sistema 📋

- [Node.js](https://nodejs.org/en/)


## Configuración 🔧

Confirmar instalación de los requerimientos del sistema.

    node -v
    npm -v

Instalar los siguientes paquetes para procesar los estilos con sus respectivos prefijos.

    npm i -D sass autoprefixer postcss postcss-cli onchange

Si ya ejecuto previamente esta instalación no es necesario volver a ejecutarla, se puede revisar que paquetes se tienen instalados localmente.

    npm list --depth=0


## Como Ejecutar 🕹️

Abrir una terminal e ingresar a la carpeta raiz del theme del proyecto, en este caso la carpeta llamada *sa_golden_ruleta_theme*.

    cd /**/**/sa_golden_ruleta_theme

Ejecutar la siguiente tarea transpilar los estilos - una vez se ejecuta queda en modo reactivo, escuchando los cambios que se generen en alguno de los archivos scss o sass.*

    npm run build

Para detener el anterior proceso solo se debe ejecutar **Ctrl + c**


## Imagenes 🗂️

_La recomendación principal en el manejo optimo de las imagenes es mantener el peso, las dimensiones y los formatos adecuados._

### Organización
- **bg:** para las imagenes de gran dimensión que correspondan al fondo de alguna sección.
- **misc:** para las imagenes pequeñas que no representen el fondo de alguna sección, generalmente recuadros, iconos, logos, capas, avatares, etc.

### Formatos
- **JPG:** para imagenes que no contengan transparencia.
- **PNG:** para imagenes que si contengan transparencia.
- **SVG:** Para imagenes que respresenten figuras y/o necesiten algun tipo de redimension sin perder calidad. (logos, iconos)

> _El formato **Webp** aun no se considera un estandar debido a que a la fecha no se encuentra soportado por todos los navegadores._

### Compresión
_Seguir las siguientes recomendaciones:_
- Tener en cuenta la dimensión original de la imagen y la dimensión en la que la misma se renderiza en el DOM, las imagenes que renderizan mucho mas pequeñas que la original pueden afectar notablemente la puntuación en los buscadores y el performance en general.
- Las imagenes no deberian sobrepasar **1MB** de peso, se puede reducir el peso sin bajar la calidad eliminando la metadata asociada - se recomienda <https://tinypng.com/> para este proceso.
- Si el proyecto no cuenta con algun metodo de carga diferida de imagenes por favor implementar, en caso de que si, tener en cuenta las etiquetas **img** con el atributo **data-src** y la clase **lazy**.


## Colaboradores 🏓

- Nicolas Muñoz <jose.munozs@ab-inbev.com>