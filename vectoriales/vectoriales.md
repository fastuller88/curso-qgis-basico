# Creación de un Mapa Básico

En este módulo, crearás un mapa básico, que se utilizará más tarde como la base para más demostraciones de las funcionalidades de QGIS.

## Contenidos

* [Trabajando con datos Vectoriales](#trabajando-con-datos-vectoriales)
    * [Paso a Paso: Viendo los Atributos de la Capa](#paso-a-paso-viendo-los-atributos-de-la-capa)
    * [Paso a Paso: Cargando Datos Vectoriales Desde Archivos Shape](#paso-a-paso-cargando-datos-vectoriales-desde-archivos-shape)
    * [Paso a Paso: Cargando Datos Vectoriales desde un Conjunto de Datos Spatialite](#paso-a-paso-cargando-datos-vectoriales-desde-un-conjunto-de-datos-spatialite)
    * [Paso a Paso: Cargando capas desde GeoPackages](#paso-a-paso-cargando-capas-desde-geopackages)
    * [Paso a Paso: Reordenando las Capas](#paso-a-paso-reordenando-las-capas)
    * [En Conclusión](#en-conclusion)
    * [¿Qué sigue a continuación?](#qué-sigue-a-continuación)
* [Simbología](#simbologia)
    * [Paso a Paso: Cambiando colores](#paso-a-paso-cambiando-colores)
    * [Inténtalo tú! Cambia el color](#inténtalo-tú-cambia-el-color)
    * [Paso a Paso: Cambiando la estructura del símbolo](#paso-a-paso-cambiando-la-estructura-del-siímbolo)
    * [Inténtalo tú! Cambia el color del estilo de marca](#inténtalo-tú-cambia-el-color-del-estilo-de-marca)
    * [Paso a Paso: Visibilidad Basada en Escala](#paso-a-paso-visibilidad-basada-en-escala)
    * [Paso a Paso: Añadiendo Capas de Símbolos](#paso-a-paso-añadiendo-capas-de-símbolos)
    * [Inténtalo tú! Cambia la textura de una capa](#inténtalo-tú-cambia-la-textura-de-una-capa)
    * [Paso a Paso: Ordenando los Niveles de Símbolos](#paso-a-paso-ordenando-los-niveles-de-símbolos)
    * [Inténtalo tú! cambia el color](#inténtalo-tú-cambia-el-color)
    <!-- * [Inténtalo tú! Cambia la apariencia de una capa](#inténtalo-tú-cambia-la-apariencia-de-una-capa) -->
    * [Paso a Paso: Tipos de Capas de Símbolos](#paso-a-paso-tipos-de-capas-de-símbolos)
        * [Tipos de Capas de Símbolos para Puntos](#tipos-de-capas-de-símbolos-para-puntos)
        * [Tipos de Capas de Símbolos para Líneas](#tipos-de-capas-de-símbolos-para-lineas)
        * [Tipos de Capas de Símbolos para Polígonos](#tipos-de-capas-de-símbolos-para-polígonos)
    * [(OPCIONAL) Paso a Paso: Creando un Relleno SVG Personalizado](#opcional-paso-a-paso-creando-un-relleno-svg-personalizado)
    * [En Conclusión](#en-conclusion)
    * [Más lecturas…](#mas-lecturas)
* [Estado de las capas](#estado-de-las-capas)
    * [Capas visibles](#capas-visibles)
    * [Capas activas](#capas-activas)
    * [Inténtalo tú! Mostrar, ocultar y activar capas.](#inténtalo-tú-mostrar-ocultar-y-activar-capas)
    * [¿Qué sigue a continuación?](#qué-sigue-a-continuación)


## Trabajando con datos Vectoriales
Los datos vectoriales son posiblemente el tipo más común de los datos que se encuentran en el uso diario de los SIG. En él se describen los datos geográficos en términos de puntos, que se puede conectar a las líneas y polígonos. Cada objeto en un conjunto de datos de vectores se llama una **característica**, y se asocia con los datos que describe esa característica.

**El objetivo de esta lección**. Aprender acerca de la estructura de los datos vectoriales, y cómo cargar un conjunto de datos vectoriales dentro de un mapa.

### Paso a Paso: Viendo los Atributos de la Capa

Es importante saber que los datos con los que estarás trabajando no solo representan **dónde** están los objetos espacialmente, sino también te dicen **qué** son esos objetos.

Desde el ejercicio anterior, deberías tener la capa `roads` cargada en tu mapa. Lo que puedes ver ahora mismo no es más que la posición de las calles.

Para ver todos los atributos de la componente temática, selecciona la capa roads en el panel de capas y haz clic con el botón derecho sobre el nombre de la capa roads y selecciona `Abrir tabla de atributos`: 

![Abrir tabla de atributos](/img/abrirAtributos.png)

Se mostrará una tabla con la información temática de la capa `roads`. Esta tabla se conoce como tabla de atributos. Las líneas que puedes ver en tu mapa representan donde van las calles; esto son los datos espaciales.

Estas definiciones se usan comúnmente en SIG, ¡por eso es esencial recordarlas!

* Ahora puedes cerrar la tabla de atributos.

Los datos vectoriales representan elementos en términos de puntos, líneas y polígonos en un plano de coordenadas. Esto es usado normalmente para guardar elementos discretos, como calles, manzanas, parques o restaurantes.

### Paso a Paso: Cargando Datos Vectoriales Desde Archivos Shape

El **Archivo Shape** es un formato específico de archivo que te permite guardar datos SIG en grupos de archivos asociados. Cada capa consiste en muchos archivos con el mismo nombre, pero diferentes tipos de archivo. 

Por ejemplo, en la carpeta `epsg4326` hay varias capas: “places”, “rivers”, “roads”, etc. Cada una de esas capas está compuesta de varios archivos: ej: roads.dbf, roads.prj, roads.shp, etc… Es importante saber que todos los archivos son necesarios para abrir la capa, por lo que si quieres copiar una capa a otra carpeta o computadora, es necesario copiar todos los archivos que tengan el mismo nombre.

![Archivos shape](/img/archivosShape.png)

Los Archivos Shape son bastante comunes pero son anticuados y en varios casos difíciles de manejar, por lo que en la actualidad se suelen trabajar con otros tipos de archivos, tales como conjuntos de datos **spatialite**, **bases de datos**, o **geopackage**. 

Si no sabes como añadir una capa vectorial, regresa al [ejercicio introductorio](/interfaz/interfaz.md#añadiendo-tu-primera-capa).
Carga las siguientes capas desde la carpeta `epsg4326` en su mapa siguiendo el mismo método:

* “places”
* “water”
* “rivers”
* “buildings”

### Paso a Paso: Cargando Datos Vectoriales desde un Conjunto de Datos Spatialite

A diferencia de los archivos shapefile, los **conjuntos de datos** te permiten guardar un gran volumen de datos asociados en un archivo. Puede que te resulte familiar un sistema de manejo de base de datos (DBMS) como Microsoft Access. Las aplicaciones SIG pueden también utilizar conjuntos de datos. SIG-específicos DBMS (como PostGIS) tienen funciones extra, ya que necesitan manejar datos espaciales. Uno de los formatos comunes de bases de datos espaciales es Spatialite, basado en el sistema de bases de datos sqlite.

* Haga clic en el administrador de fuentes de datos ![Añadir capa](/img/addLayer.png) 

(Si estas seguro de no poder verlo en absoluto, comprueba que la `barra de herramientas del proyectoestá activada`.)

En la ventana del administrador, seleccionar en la sección de la izquierda, “SpatiaLite”. Se abrirá la opción “Conexiones”. 

* Clica el botón `Nueva`.
* En la misma carpeta `epsg4326`, debe encontrar el archivo `landuse.sqlite`. Selecciónelo y haga clic en `Abrir`.

Ahora verá nuevamente la sección de “Conexiones”. Tenga en cuenta que el menú desplegable seleccionado antes de los tres botones ahora lee “landuse.sqlite@...”, seguido por la ruta del archivo de base de datos en su computadora.

Clica en el botón `Conectar`. Deberías ver esto en la siguiente caja vacía:

![SpatiaLite](/img/spatiaLite.png) 

Clica en la capa `landuse` para seleccionarla, y clica `Añadir`. En el caso que surja un nuevo cuadro de diálogo del “selector del sistema de coordenadas” escriba 4326 en el campo “filtrar” y escoja WGS84 en “Sistemas de referencia de coordenadas del mundo” (más adelante se explicarán mejor estos conceptos”.

![Sistema de referencia de coordenadas](/img/src.png) 

> Nota: ¡Recuerda guardar el mapa a menudo! El archivo del mapa no contiene ninguno de los datos directamente, pero recuerda qué capas cargaste dentro de tu mapa.


### Paso a Paso: Cargando capas desde GeoPackages

Uno de los formatos más avanzados para almacenamiento de datos geográficos el el formato GeoPackage. Este formato también está basado en SpatiaLite, pero permite en un solo archivo gestionar datos, estilos de simbología, proyectos de QGIS, y muchas otras cosas. Es muy conveniente ya que en un solo archivo se puede almacenar todo y abrirlo en diferentes tipos software. Además evita el problema de trasladar archivos y carpetas entre diferentes computadores y facilita los respaldos.

* Inicia un proyecto nuevo de QGIS y abre el panel de navegador.
* Navega hasta tu carpeta de datos y  abre la carpeta `epsg32717`. Encontrarás un archivo area_estudio. 

> Nota: si no tienes éste archivo, puedes descargarlo la carpeta con los datos directamente desde  el siguiente enlace: [trainingdata_QGIS](https://github.com/fastuller88/curso-qgis-basico/raw/master/data/trainingdata_QGIS.zip). Debes descomprimir el archivo en una carpeta en tu disco duro  antes de comenzar a trabajar.

* Este archivo es una base de datos geopackage. Haz click en la flecha desde el panel de navegador de QGIS para desplegar sus contenidos

* Verás que contiene las mismas capas que están en la otra carpeta como shapefile.

![Importar geopackage](/img/geopackage.png) 

* Haz doble click en cada capa para añadirla al mapa. Verás que las añadidas tienen ya una simbología asignada, ya que fueron guardadas con su simbología en la base de datos geopackage.

![Capas cargadas desde geopackage](/img/capasCargadas.png) 

### Paso a Paso: Reordenando las Capas

Las capas en tu lista de Capas están dibujadas en el mapa en cierto orden. La capa de abajo de la lista está dibujada primero, y la capa de la parte superior de la lista es la última dibujada. Cambiando el orden de la lista, puedes cambiar el orden en el que dibujan en el mapa.

El orden en el que las capas se han cargado en el mapa probablemente no sea lógico en este punto. Es posible que la capa roads esté completamente escondida porque otras capas estén por encima de ella.

Para resolver este problema:

* Clica y arrastra sobre una capa y arrastrala en la lista de Capas. La norma general es que los capas tipo polígono vayan al fondo de la lista, luego las capas tipo línea y por encima los puntos.

![Capas ordenadas](/img/leyendaOrdenada.png) 

Verás que el mapa ahora tiene más sentido visual, con calles y construcciones apareciendo sobre las regiones del territorio.

### En Conclusión

Ahora has añadido todas las capas que necesitas desde muchas fuentes diferentes.

### ¿Qué sigue a continuación?

Utilizando la paleta aleatoria asignada automáticamente cuando cargas las capas, tus mapas actuales probablemente no sean fáciles de leer. Sería preferible asignar tu propia elección de colores y símbolos. Esto es lo que aprenderás a hacer en la siguiente lección.

## Simbología

La simbología de una capa es su apariencia visual en el mapa. La fortaleza básica del SIG sobre otras formas de representación de datos espaciales es que con el SIG, puedes obtener una representación visual dinámica de los datos con los que estás trabajando.

Además, la apariencia visual del mapa (la cual depende de la simbología de las capas individuales) es muy importante. El usuario final de los mapas que tú produces necesitará ver lo que el mapa representa con facilidad. De la misma forma, necesitarás ser capaz de explorar los datos con los que trabajas, y una buena simbología ayuda mucho.

En otras palabras, tener una buena simbología no es solo un lujo o simplemente bonito. De hecho, es esencial para ti usar el SIG adecuadamente y producir mapas e información que la gente pueda usar.

**El objetivo de esta lección**: Ser capaz de crear cualquier simbología que quieras para una capa vectorial.

### Paso a Paso: Cambiando colores

Para cambiar la simbología de una capa, abre su `Propiedades de la capa`. Empieza cambiando el color de la capa `landuse`.

* Clic derecho en la capa landuse en el panel de capas.
* Selecciona Propiedades en el menú que aparece.

> Nota: Por defecto, también puedes acceder a las propiedades de la capa con doble clic en la capa en la lista de capas.

En la ventana de `Propiedades`:

* Selecciona la pestaña `Simbología` en el menú izquierdo:

![Simbología](/img/accediendoSimbologia.png) 

* Clic en el botón de selección del color al lado de la etiqueta `Color`.

Un diálogo estándar de color aparecerá.

* Escoge el color gris y clic en `Aceptar`.
* Clic de nuevo en `Aceptar` en la ventana `Propiedades de la capa`, y verás el cambio de color en la capa.

### :pencil2: Inténtalo tú! Cambia el color

* Cambia el color de la capa water a azul claro.
* Comprueba que la capa water tiene el nuevo color que le has asignado.

### Paso a Paso: Cambiando la estructura del símbolo

De momento está bien, pero hay más simbología en una capa además del color. Lo siguiente que queremos es eliminar las líneas entre las diferentes áreas de uso para que el mapa no esté tan visualmente desordenado.

* Abre la ventana `Propiedades` de la capa para la capa `landuse`.

Bajo la pestaña `Simbología`, verás el mismo tipo de diálogo que antes. Esta vez, sin embargo, harás más que cambiar rápidamente el color.

* En el la sección de estructura del símbolo, expande el desplegable `Relleno` de ser necesario y selecciona la opción `Relleno sencillo (Simple fill)`.
* Clic en el desplegable `Estilo de marca (Stroke style)`. En este momento, debería mostrar `“Línea sólida”`.
* Cámbialo a `Sin plumilla`.
* Clic en `Aceptar`.


![Sin plumilla](/img/sinPlumilla.png) 

Ahora los polígonos de la  capa landuse no tendrán borde y la representación visual será mejor.

### Inténtalo tú! Cambia el color del estilo de marca

* Cambia la simbología de la capa water otra vez para que tenga un trazado externo azul oscuro.
* Cambia la simbología de la capa rivers para una representación más acorde con los ríos.

>Si tu eres un usuario principiante, puede detenerse aquí.
>
>* Use el método anterior para cambiar los colores y estilos a todas las capas restantes.
>* Trate de usar colores naturales para los objetos. Por ejemplo, una carretera no debería ser roja o azul, pero si puede ser gris o negro.
>* También siéntete libre de experimentar con diferentes `Estilos de Relleno` y `Estilos de borde o estilo de marca` ajustados para polígonos.

### Paso a Paso: Visibilidad Basada en Escala

Algunas veces encontrarás que una capa no es adecuada para una escala dada. Por ejemplo, un conjunto de datos de todos los continentes puede tener pocos detalles, y no ser muy preciso a nivel de calles. Cuando esto ocurre, quieres ser capaz de ocultar el conjunto de datos a escalas inapropiadas.

En nuestro caso, puede que decidamos ocultar las construcciones vistas a pequeñas escalas. Este mapa, por ejemplo...

![Simbología a escala](/img/simbologiaEscala.png) 

... no es muy útil. Las construcciones difícilmente se distinguen a esa escala.

Para habilitar la representación basada en escala:

* Abre el diálogo `Propiedades de la capa` para la capa `buildings`.
* Activa la pestaña `Representación`.
* Habilite la representación basada en escala haciendo clic en la casilla de verificación llamada `Visibilidad dependiente de la escala`:

![Simbología a escala mínimo](/img/simbologiaEscalaMin.png) 

* Cambie el valor Mínimo a 1:10.000.
* Clic en Aceptar.

Comprueba los efectos de esto aumentando y disminuyendo el zoom de tu mapa, notando que la capa buildings aparece y desaparece.

> Nota: Puedes usar la rueda de tu ratón para ampliar o disminuir el zoom. También puedes utilizar las herramientas de zoom para ampliar el mapa usando un recuadro:
>
> ![Zoom](/img/zomInOut.png)  

### Paso a Paso: Añadiendo Capas de Símbolos

Ahora sabes como cambiar la simbología simple de capas, el siguiente paso es crear simbología más compleja. QGIS te permite hacer esto utilizando capas de símbolos.

* Regrese al panel de propiedades de símbolos `landuse` (haga clic Relleno sencillo en el panel `Capas de símbolos`).

En este ejemplo, los símbolos actuales no tienen contorno (es decir, usan el estilo de borde `Sin plumilla`)

Selecciona `Relleno sencillo` en la opción `Tipo de capa del símbolo`. Después clic en el botón Añadir capa de símbolos: ![Añadir](/img/anadir.png)  

* Clícalo y el diálogo cambiará para parecerse a algo como esto:

![Añadir capa de símbolo](/img/anadirCapaSimbolo.png) 

(Por ejemplo, puede que aparezca de diferente color, pero tú vas a cambiarlo de todos modos.)

Ahora hay una segunda capa de símbolos. Siendo un color sólido, por supuesto esto ocultará completamente el anterior tipo de símbolo. Además, tiene el `Wstilo de marca` `Línea sólida`, lo que no queremos. Claramente este símbolo tiene que ser cambiado.

>Nota: Es importante no confundirse entre una capa de mapa y una capa de símbolos. Una capa de mapa es un vector (o raster) que ha sido cargada dentro del mapa. Una capa de símbolos es parte de un símbolo utilizado para representar una capa del mapa. Este curso se referirá por lo general a capas del mapa como una capa, pero una capa de símbolos siempre será llamada capa de símbolos, para prevenir confusión.

Con la nueva capa `Relleno sencillo` seleccionada:

* Ajusta el estilo de borde a `Sin plumilla`, como antes.
* Cambia el estilo de relleno a algo diferente a `Sólido` o `Sin relleno`. Por ejemplo `Diagonal` o `Denso`:

![Añadir capa de símbolo denso](/img/capaSimboloDenso.png) 

* Clic en Aceptar. Ahora puedes ver tus resultados y ajustarlos como necesites.

Puedes incluso añadir múltiples capas de símbolos extra y crear un nuevo tipo de textura para tu capa de este modo.

![Añadir varios capa de símbolo](/img/capaSimboloVarios.png) 

¡Es divertido! Pero probablemente tenga demasiados colores para usar en el mapa real...

### :pencil2: Inténtalo tú! Cambia la textura de una capa

* Recordando ampliar si es necesario, crea una textura simple para la capa `buildings` utilizando los métodos anteriores.

> Personaliza tu buildings capa como gustes, pero recuerda que tiene que ser fácil de contar las diferentes partes del mapa y verse genial :sunglasses:

### Paso a Paso: Ordenando los Niveles de Símbolos

Cuando las capas de símbolos están representadas, también están representadas en una secuencia, similar a la forma en la que diferentes capas del mapa se representan. 

Por ejemplo, queremos dar a las calles un símbolo como este:![Calles](/img/street.png). Este es un símbolo compuesto por dos “capas de símbolos”. La primera capa es una línea negra gruesa y la segunda capa una línea blanca de guiones.

* En la capa `roads` una capa símbolo extra (utilizando el método para añadir capas símbolo demostrado anteriormente).
* Dale a la nueva capa de símbolo superior un `Ancho de marca` de 0.2, color blanco y selecciona `Línea de guiones` del menú desplegable `Estilo de plumilla (Stroke style)`.
* Dale a la capa de símbolo inferior un grosor de 1.3 y asegúrate de que es una `Línea sólida`.

![Añadir varios capa de símbolo vías](/img/capaSimboloVarios.png) 

>Si cambias el orden de las capas de símbolo notarás que la línea negra sólida cubre a la línea blanca de guiones y no se visualiza correctamente. Para prevenir que esto ocurra, puedes ordenar los niveles de símbolos y de este modo controlar el orden en el que las diferentes capas de símbolos se representan.
Para cambiar el orden de la capa de símbolos, seleccione la línea blanca de guiones en el estilo de la capa y haga click en el botón “subir” para colocarla sobre la línea negra.

![Añadir varios capa de símbolo vías vista](/img/capaSimboloVistaVias.png) 

Cuando hayas terminado, recuerda guardar el símbolo para no perder tu trabajo si lo vuelves a cambiar en el futuro. Puedes guardar tu actual estilo de símbolo con clic en el botón `Guardar estilo` bajo el botón  `Estilo` que se encuentra en la parte inferior izquierda del cuadro de diálogo. Generalmente, deberías guardar como `Archivo de estilo de capa de QGIS`.

Guarda tu estilo en `trainingdata_QGIS/styles`. Puedes cargar estilos guardados previamente en cualquier momento con clic en el botón `Cargar estilo`.... Antes de cambiar un estilo, ten en mente que cualquier estilo no guardado que reemplaces se perderá.

### :pencil2: Inténtalo tú! Cambia la apariencia de una capa

* Cambia de nuevo la apariencia de la capa `roads`. Las calles deben ser estrechas y grises, con un fino contorno amarillo.



