# 5. Módulo: Creación de Mapas

En este módulo aprenderás cómo usar el Diseñador de Mapas de QGIS para producir mapas de calidad con todos los elementos de mapa que son requisito.

## Contenidos

* [5. Módulo: Creación de Mapas](#5-módulo-creación-de-mapas)
    * [5.1. Lección: Utilización del Diseñador de Mapas](#51-lección-utilización-del-diseñador-de-mapas)
        + [5.1.1. Paso a Paso: El Administrador de composiciones](#511-paso-a-paso-el-administrador-de-composiciones)
        + [5.1.2. Paso a Paso: Composición Básica del Mapa](#512-paso-a-paso-composición-básica-del-mapa)
        + [5.1.3. Paso a Paso: Añadiendo un Título](#513-paso-a-paso-añadiendo-un-título)
        + [5.1.4. Paso a Paso: Añadiendo una Leyenda](#514-paso-a-paso-añadiendo-una-leyenda)
        + [5.1.5. Paso a Paso: Personalizando Elementos de la Leyenda](#515-paso-a-paso-personalizando-elementos-de-la-leyenda)
        + [5.1.6. Paso a Paso: Exportando Tu Mapa](#516-paso-a-paso-exportando-tu-mapa)
        + [5.1.7. En Conclusión](#517-en-conclusión)
        + [5.1.8. ¿Qué sigue a continuación?](#518-qué-sigue-a-continuación)
    * [5.2. Añadiendo y personalizando la barra de escala.](#52-añadiendo-y-personalizando-la-barra-de-escala)
    * [5.3. Ejercicio 1](#53-ejercicio-1)
    * [5.3.1. En Conclusión](#531-en-conclusión)

## 5.1. Lección: Utilización del Diseñador de Mapas

Al crear un mapa, normalmente necesitas imprimirlo o exportarlo a un documento. Recordemos que el archivo de proyecto de SIG guarda el estado del programa SIG, con referencias a todas las capas, sus etiquetas, colores, etc. Así que para alguien que no tenga los datos o QGIS, el archivo del mapa será inútil. Afortunadamente, QGIS puede exportar el archivo del mapa a un formato gráfico que cualquier ordenador pueda leer, así como imprimir el mapa en una impresora. Exportar e imprimir se realiza a través del **Diseñador de Mapas** (También llamado **Diseñador de Impresión**).

**El objetivo de esta lección**: Utilizar el Diseñador de Mapas del QGIS para crear un mapa básico en formatos gráficos para exportación e impresión.

> NOTA: Si has completado los pasos anteriores del tutorial, debes tener algunas capas cargadas con su respectiva representación. De lo contrario puedes descargarte un archivo de mapa listo. Alternativamente, puedes cargar tus propias capas y darles una representación adecuada.
> 
> Si no lo has hecho aún descarga el archivo comprimido con los datos para éste curso haciendo click en el siguiente enlace: [trainingdata_QGIS](https://github.com/fastuller88/curso-qgis-basico/raw/master/data/trainingdata_QGIS.zip). Debes descomprimir el archivo en una carpeta en tu disco duro antes de comenzar a trabajar.
> 
> * Ve a la ubicación  `trainingdata_QGIS/proyectos/`.
> * Abre el archivo `general.qgz` en QGIS. Si todo está bien debería aparecerte con las siguientes capas o algo parecido. De lo contrario es posible que tengas que buscar las capas manualmente.

![Mapa terminado](/img/mapaTerminado.png)

### 5.1.1. Paso a Paso: El Administrador de composiciones

QGIS te permite crear múltiples mapas utilizando el mismo archivo de mapa. Por esta razón, tiene una herramienta llamada `Administrador de composiciones`.

* Haz clic en el menú `Proyecto ‣ Administrador` de composiciones para abrir esta herramienta. También puedes usar el botón “Administrador de composiciones” en la barra de herramientas.

![administradorCopmposiciones](/img/administradorCopmposiciones.png)

* Verás aparecer el `Administrador de composiciones`.
* Haz clic en el botón `Crear` y da al nuevo diseñador el nombre “Mi primera composición”.
* `Haz clic en Aceptar`.

Ahora el diseñador estará disponible en el menú  `Proyecto ‣ Composiciones`,

Cualquier ruta que escojas te llevará ahí, verás ahora la ventana `Diseñador de impresión`:

![Diseñador de impresión](/img/disenadorImpresion.png)

### 5.1.2. Paso a Paso: Composición Básica del Mapa

En este ejemplo, el mapa ya está representado con la simbología que queremos. Para este ejercicio puedes utilizar el mapa con las capas disponibles o cargar tus propias capas.

* Haz click con el botón derecho sobre la página vacía y selecciona `Propiedades de la Página` y en la pestaña `Propiedades del elemento` comprueba que las opciones están ajustados como sigue:
    * `Tamaño`: A4 (210x297mm)
    * `Orientación`: Horizontal

![disenadorImpresionPropiedades](/img/disenadorImpresionPropiedades.png)

En la pestaña `Diseño`, comprueba los valores de `Configuración de exportación` 

* `Resolución de exportación`: 300dpi

Ahora tienes listo una página A4 en blanco para exportar o imprimir a una resolución de 300ppi. A continuación agregaremos los elementos del mapa a la página.

* Haz clic en el botón `Añadir nuevo mapa`: ![anadirNuevoMapa](/img/anadirNuevoMapa.png)

Con esta herramienta activada se colocará el mapa en la página.

* Haz clic y arrastra un rectángulo en la página en blanco:

![anadirNuevoMapaRec](/img/anadirNuevoMapaRec.png)

El mapa aparecerá en la página.

* Mueve el mapa clicando y arrastrándolo:

![composicionMapaAgreagado](/img/composicionMapaAgreagado.png)

Cambia el tamaño clicando y arrastrando sobre las esquinas del rectángulo. Ajusta el contenido del mapa a la página dejando márgenes pequeños a todos los lados y un espacio arriba para el título.

> Nota: Es posible que tu mapa se vea muy diferente, ¡Por supuesto! Esto depende en cómo está ajustado tu propio proyecto. ¡Pero no te preocupes! Estas instrucciones son generales, así que funcionarán adecuándose a la forma en que se vea el mapa.

* Asegúrate de ajustar los márgenes a lo largo de las esquinas, y dejar un espacio en la parte superior para el título.
* Puedes alejar o acercar la página con los siguientes botones. Esto no cambiará el contenido del mapa.: ![acercarPagina](/img/acercarPagina.png)

De forma predeterminada, el contenido del mapa en la página muestra exactamente lo que se está visualizando en el lienzo del mapa en la ventana principal de QGIS.

* Para desplazar el contenido del mapa se utiliza la herramienta Mover contenido del elemento: ![desplazarComposicion](/img/desplazarComposicion.png)
* Para cambiar la escala del mapa, debes tener seleccionado el mapa en la página. Luego ir a la pestaña `Propiedades del elemento > Propiedades principales` y en el cuadro escala colocar la escala deseada. 
* Coloca el mapa a una escala de 10000 y muévelo para representar la zona central de la ciudad.

![composicionEscala](/img/composicionEscala.png)

Cuando amplíes, el mapa no se actualizará por sí mismo. Así que no pierdas el tiempo dibujando de nuevo el mapa mientras amplíes la página a donde quieras, también significa que si amplías o disminuyes el zoom, el mapa estará en una incorrecta resolución y se verá mal o será ilegible.

* Cuando hagas cambios actualiza el mapa clicando el botón: ![actualizar](/img/actualizar.png)

Recuerda que el tamaño y posición que te da el mapa no son la final necesariamente. Siempre puedes volver y cambiarla si no te satisface. Por ahora, necesitas asegurarte que has guardado tu trabajo en el mapa. Como un `Diseñador` en QGIS es parte de un archivo de mapa principal, necesitarás guardar tu proyecto principal. Vas a la ventana QGIS principal (la que tiene Lista de capas y los otros elementos familiares con los que has estado trabajando), y guarda tu proyecto desde el menú `Proyecto > Guardar como...`

### 5.1.3. Paso a Paso: Añadiendo un Título

Ahora tu mapa se ve bien en la página. Pero un mapa tiene más que el contenido geográfico: Suelen tener título, leyenda, escala, etc. Todos estos elementos se conocen como “información marginal” del mapa. Primero, añadamos un título.

* Haz clic en el botón “Añadir etiqueta”: ![anadirEtiqueta](/img/anadirEtiqueta.png). Una etiqueta es cualquier elemento de texto en la información marginal del mapa.
* Haz clic en la página, arriba del mapa, y una etiqueta aparecerá en la parte superior del mapa.
* Cambia el tamaño y sitúala en el centro superior de la página. Puede cambiarse de tamaño y ser movido de la misma forma que el mapa.

Cuando muevas el título, notarás que aparecen líneas guía para ayudarte a posicionarlo en el centro de la página.
Sin embargo, también hay una herramienta para posicionar el título de forma relativa a otros elementos

* Haz clic en el mapa para seleccionarlo.
* Mantén pulsado `shift` en tu teclado y clic en la etiqueta para que queden la etiqueta y el mapa seleccionados.
* Busque el botón `Alinear` ![alinear](/img/alinear.png) y haga clic en la flecha del menú desplegable junto a él para revelar las opciones de posición y haga clic en `Alinear al centro`:

![alinearCentro](/img/alinearCentro.png)

Podrás observar que en el lado derecho, en el panel de `Elementos` se van listando todos los elementos que añades a la composición. En la lista de elementos, puedes ocultar o mostrar cada elemento y puedes bloquearlos para que no se muevan accidentalmente. 

![elementosBloqueados](/img/elementosBloqueados.png)

* Bloquea el mapa y la etiqueta del título.

Ahora la etiqueta está centrada en el mapa, pero los contenidos no lo están. Para centrar los contenidos de la etiqueta:

* Selecciona la etiqueta clicando en ella.
* Haz clic en la pestaña `Propiedades del elemento` del panel lateral de la ventana del `Diseñador`.
* Cambia el texto de la etiqueta a "MI PRIMERA COMPOSICION":
* Utiliza la interfaz para ajustar las opciones de alineación y tipo de letra:

![tituloApariencia](/img/tituloApariencia.png)

* Elige un tipo de letra grande pero discreto (por ejemplo usa la fuente ARIAL con un tamaño de 36) y ajusta la Alineación horizontal a Centro. y `Alineación horizontal` a `Medio`.

También puedes cambiar el color de la fuente, pero probablemente sea mejor mantenerla en negro como por defecto. Los ajustes por defecto no añaden un marco a la caja de texto del título, si quieres añadir un marco, puedes hacerlo así:

* En la pestaña `Propiedades del elemento`, desplázate hacia abajo hasta que veas la opción `Marco`.
* Haz clic en la casilla de verificación para habilitar el marco. También puedes cambiar el color del marco y su grosor. También puedes cambiar el fondo

![composicionMarcoTitulo](/img/composicionMarcoTitulo.png)

### 5.1.4. Paso a Paso: Añadiendo una Leyenda

Quien lea el mapa también necesita ser capaz de ver qué significan las cosas representadas en el mapa. En algunos casos, como los nombres de los sitios, es muy obvio. En otros casos es más difícil de adivinar, como los usos del suelo. Así que añadamos una leyenda nueva:

* Haz clic en este botón en la barra: ![anadirLeyenda](/img/anadirLeyenda.png)
* Haz clic en la página para situar la leyenda, y muévela hasta donde quieras situarla.

![leyendaComposicion](/img/leyendaComposicion.png)

### 5.1.5. Paso a Paso: Personalizando Elementos de la Leyenda

No necesitamos todo lo que está en la leyenda, así que eliminaremos los elementos no deseados.

* En la pestaña `Propiedades del elemento`, encontrarás el panel `Elementos de la leyenda`.
* Desactiva la opción “auto actualizar”.
* Busca y selecciona `buildings` en el panel inferior.
* Eliminelo de la leyenda haciendo clic en el botón `menos`.
* Repite el proceso para eliminar `rivers`, `water` y `places`.

![propiedadesElementoLeyenda](/img/propiedadesElementoLeyenda.png)

* Vuelve a añadir a la leyenda la capa `buildings` con el botón  más.

También puedes renombrar los elementos que aparecen en la leyenda:

* Selecciona `roads` en la lista de elementos de la leyenda.
* Haz clic en el botón `Editar`: ![editarLeyenda](/img/editarLeyenda.png)
* Renombra la capa a `Vías`.
* Renombra la capa `landuse` a “Uso del Suelo”. Haz clic en la flecha hacia abajo y edita cada categoría para renombrarlas a español.
* Repite el proceso para eliminar de la capa “vías” todas las categorías que incluyen “link”. Además renombra las categorías de calles a español.
* También puedes reordenar los elementos de la leyenda.

![leyendaRenombrada](/img/leyendaRenombrada.png)

Como la leyenda cambiará de anchura con los nuevos nombres de capas, puede que desees mover y cambiar el tamaño de la leyenda y/o el mapa. Además, puedes colocar un título de la leyenda, cambiar el tipo de letra, añadir un borde o fondo, etc.

Este es el resultado

![composicionFinal](/img/composicionFinal.png)

### 5.1.6. Paso a Paso: Exportando Tu Mapa

> Nota: ¿Te acordaste de guardar tu trabajo regularmente?

¡Finalmente el mapa está listo para exportarlo! Verás los botones de exportación en la esquina superior izquierda de la ventana `Diseñador`.

![imprimirMapa](/img/imprimirMapa.png)

El botón de la izquierda es `Imprimir`, que se enlaza con la impresora. Las opciones de impresión cambiarán dependiendo del modelo de impresora con la que trabajes, probablemente sea mejor consultar el manual de la impresora o una guía general de impresión para más información sobre este tema.

Los otros tres botones te permiten exportar la página del mapa a un archivo. Hay tres formatos entre los que elegir:

* Exportar como imagen
* Exportar como SVG
* Exportar como PDF

Exportar como una imagen te dará una selección de varios formatos de imagen comunes a elegir. Es probablemente la opción más simple, pero la imagen creada está “muerta” y es difícil de editar.

Las otras dos opciones son más comunes.

Si va a enviar el mapa a un cartógrafo (que desee editar el mapa para publicarlo), es mejor exportarlo como SVG. SVG significa “Gráfico de Vectores Escalares”, y puede ser importado a programas como Inkscape u otro software de edición de imágenes vectoriales.

Si vas a mandar el mapa a un cliente, es más común utilizar un PDF, ya que es más fácil de usar y de ajustar las opciones de impresión. También algunos cartógrafos pueden preferirlo, si tienen programas que les permita editar este formato.

Para nuestros propósitos, utilizaremos PDF.

* Haga clic en el botón `Exportar como PDF`.
* Elige un destino para guardar y nombra el archivo como normalmente.
* Haz clic en Guardar.

### 5.1.7. En Conclusión

* Cierra la ventana Diseñador.
* Guarda tu mapa.
* Encuentra tu PDF exportado utilizando el administrador de archivos de tu sistema operativo.
* Ábrelo.
* Si te convence estará listo, caso contrario puedes volver a edtiar hasta que que quedes convencido.

¡:tada: Felicitaciones  por tu primer proyecto de mapa QGIS completado!

### 5.1.8. ¿Qué sigue a continuación?

En la siguiente sección, te daremos tareas para completar. Esto te permitirá practicar con las técnicas que has aprendido hasta ahora.

## 5.2. Añadiendo y personalizando la barra de escala.

Hasta ahora has utilizado el diseñador de impresión para añadir un mapa con su respectivo título y leyenda. En esta sección, deberás explorar por tí mismo las funcionalidades para añadir a la composición otro elemento importante: la barra de escala.

* Haz clic en el botón de la barra de herramientas de la izquierda: ![anadirEscala](/img/anadirEscala.png) .
* Siguiendo la misma lógica que para añadir una leyenda, agrega la barra de escala al mapa y explora las posibilidades de personalización.
* Puedes encontrar más información en el siguiente enlance: [composer_scale_bar](https://docs.qgis.org/2.14/es/docs/user_manual/print_composer/composer_items/composer_scale_bar.html)
* Añadir la flecha de norte en un mapa es fácil, pero aprovecharemos esta ocasión para que busques en internet cómo hacerlo.

## 5.3. Ejercicio 1

Abre tu proyecto de mapa existente y revísalo a fondo. Si notas algún error pequeño o cosas que te hubiera gustado solucionar antes, hazlo ahora.

Mientras personalizas tu mapa, sigue preguntándote cosas a ti mismo. ¿És el mapa fácil de leer y entender para alguien que no esté familiarizado con los datos? Si viera el mapa en internet, o en un póster, o una revista, ¿Atraería my atención? ¿Querría leer este mapa si no fuera mío?

Si estás haciendo este curso en un nivel Básico  o Intermedio , lee técnicas de secciones más avanzadas. Si ves algo que te gustaría hacer en tu mapa, ¿Por qué no intentas implementarlo?

Si te están presentando el curso, el presentador puede querer que entregues una versión final de tu mapa, exportado a PDF, para evaluarlo. Si estás haciendo el curso por ti mismo, es recomendable que te evalúes tu mismo utilizando el mismo criterio. Tus mapas serán evaluados respecto a la apariencia general de la simbología y el propio mapa, así como la apariencia y la disposición de la página del mapa y sus elementos. Recuerda que el énfasis en la evaluación de la apariencia del mapa siempre será en facilidad de uso. Cuanto mejor se vea el mapa y más fácilmente se entienda con un simple vistazo, mejor.

¡Feliz personalización!

### 5.3.1. En Conclusión

Los primeros cuatro módulos te han enseñado a crear y dar estilo a un mapa vectorial. En los próximos cuatro módulos, aprenderás a usar QGIS para un análisis completo SIG. Esto incluye crear y editar datos vectoriales; analizar datos vectoriales; utilizar y analizar datos raster; y utilizar SIG para solucionar un problema de principio a fin, utilizando tanto fuentes de datos raster como vectoriales.



