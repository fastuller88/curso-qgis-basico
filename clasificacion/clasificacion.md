# 4. Módulo: Clasificación de Datos Vectoriales

La clasificación de datos vectoriales te permite asignar diferentes símbolos a elementos (diferentes objetos en la misma capa), en función de sus atributos. Esto permite a alguien que use el mapa, ver fácilmente los atributos de distintos elementos.

## Contenidos

* [4. Módulo: Clasificación de Datos Vectoriales](#4-módulo-clasificación-de-datos-vectoriales)
    - [4.1. Lección: Datos de Atributo](#41-lección-datos-de-atributo)
        - [4.1.1. Paso a Paso: Datos de atributo](#411-paso-a-paso-datos-de-atributo)
        - [4.1.2. En Conclusión](#412-en-conclusión)
        - [4.1.3. ¿Qué sigue a continuación?](#413-qué-sigue-a-continuación)
    - [4.2. Lección: La Herramienta de Etiquetas](#42-lección-la-herramienta-de-etiquetas)
        + [4.2.1. Paso a Paso: Utilizando Etiquetas](#421-paso-a-paso-utilizando-etiquetas)
        + [4.2.2. Paso a Paso: Cambiando Opciones de Etiquetado](#422-paso-a-paso-cambiando-opciones-de-etiquetado)
        + [4.2.3. Paso a Paso: Utilizando Etiquetas en lugar de Capas de Simbología](#423-paso-a-paso-utilizando-etiquetas-en-lugar-de-capas-de-simbología)
        + [4.2.4. Inténtalo tú! Personalizar las Etiquetas](#424-pencil2-inténtalo-tú-personalizar-las-etiquetas)
        + [4.2.5. Paso a Paso: Etiquetando Líneas](#425-paso-a-paso-etiquetando-líneas)
        + [4.2.6. Paso a Paso: Ajustes Definidos de Datos](#426-paso-a-paso-ajustes-definidos-de-datos)
        + [4.2.7. Inténtalo tú! Utilizando Ajustes Definidos de Datos](#427-pencil2-inténtalo-tú-utilizando-ajustes-definidos-de-datos)
        + [4.2.8. Más Posibilidades Con Etiquetas](#428-más-posibilidades-con-etiquetas)
        + [4.2.9. En Conclusión](#429-en-conclusión)
        + [4.2.10. ¿Qué sigue a continuación?](#4210-qué-sigue-a-continuación)
    - [4.3 Lección: Clasificación](#43-lección-clasificación)
        + [4.3.1. Paso a Paso: Clasificación de Datos Nominales](#431-paso-a-paso-clasificación-de-datos-nominales)
        + [4.3.2. Inténtalo tú! Más Clasificación](#432-pencil2-inténtalo-tú-más-clasificación)
        + [4.3.3. Paso a Paso: Clasificación por Ratios](#433-paso-a-paso-clasificación-por-ratios)
        + [4.3.4. Inténtalo tú! Refinar la Clasificación](#434-pencil2-inténtalo-tú-refinar-la-clasificación)
        + [4.3.5. Paso a Paso: Clasificación basada en Reglas](#435-paso-a-paso-clasificación-basada-en-reglas)
        + [4.3.6. En Conclusión](#436-en-conclusión)
        + [4.3.7. ¿Qué sigue a continuación?](#437-qué-sigue-a-continuación)

## 4.1. Lección: Datos de Atributo

Hasta ahora, ninguno de los cambios que hemos hecho en el mapa han influido a los objetos que están siendo mostrados. En otras palabras, todos los polígonos que representan usos del suelo tienen el mismo color, y todas las calles se ven igual. Cuando se mira el mapa, los observadores no saben nada sobre las calles que están viendo; solo que hay una calle de una forma determinada en una determinada área.
Pero la fortaleza del SIG es que todos los objetos son visibles en el mapa también tienen atributos. Los mapas en un SIG no son solo imágenes. No solo representan objetos ni sitios, si no también información sobre esos objetos. Debemos recordar que la información geográfica tiene una componente espacial (los elementos geométricos representados en el mapa) y una componente temática (los atributos de esos elementos geométricos)

**El objetivo de esta lección**: Explorar los atributos de un objeto espacial y entender para qué pueden ser útiles los datos.

### 4.1.1. Paso a Paso: Datos de atributo

Abre la tabla de atributos para la capa `places` (referida atrás en la sección [3.1. Lección: Trabajando con datos Vectoriales](/vectoriales/vectoriales.md#31-lección-trabajando-con-datos-vectoriales) si es necesario) ¿Qué campo sería el más útil para presentar etiquetas con información sobre cada lugar? y ¿por qué?

>El campo name es el más útil para presentarlo como etiqueta. Esto es porque todos los valores son únicos para cada objeto y es muy poco probable que contengan valores NULL. Si tus datos tienen algunos valores NULL, no te preocupes siempre y cuando sus lugares tengan nombre.

### 4.1.2. En Conclusión

Ahora sabes como usar la tabla de atributos para ver qué hay realmente en los datos que estas usando. Cualquier conjunto de datos solo te será útil si tiene los atributos que te interesan. Si sabes qué atributos necesitas, puedes rápidamente decidir si serás capaz de utilizar un conjunto de datos dado, o si necesitas buscar otro que contenga los datos requeridos.

### 4.1.3. ¿Qué sigue a continuación?

Atributos diferentes son útiles para objetivos diferentes. Algunos de ellos pueden estar representados directamente como texto para ser visto por el usuario. Aprenderás a hacerlo en la siguiente lección.

## 4.2. Lección: La Herramienta de Etiquetas

Las etiquetas se pueden añadir a un mapa para mostrar información sobre un proyecto. Cualquier capa vectorial puede tener etiquetas asociadas a él. Esas etiquetas se basan en los datos de atributo de una capa para su contenido.

>Nota: El cuadro de diálogo `Propiedades de la capa` tiene una pestaña `Etiquetas` que ofrece la misma función, pero para este ejemplo utilizaremos la `Herramienta de etiquetado de capa`, accediendo a través del botón de la barra de herramientas.

**El objetivo de esta lección**: Aplicar etiquetas útiles y que queden bien en una capa.

### 4.2.1. Paso a Paso: Utilizando Etiquetas

Antes de ser capaz de acceder a la herramienta de Etiquetas, necesitarás asegurarte de que está activada.

* Ve al elemento del menú `Ver ‣ Barra de Herramientas`
* Asegúrate de que el elemento `Barra de herramienta` de `Etiqueta` está marcado, de lo contrario, actívalo.
* Haz clic en la capa `places` en la `Lista de capas`, para que quede resaltado.
* Haga clic en el botón `Opciones de etiquetado de capa` de la barra de herramientas: ![Herramienta etiquetado](/img/herramientaEtiquetado.png)

Esto te abrirá el cuadro de diálogo `Configuración del etiquetado de la capa`.

* De la lista elige `Etiquetas sencillas`.
* Marca el cuadro junto a `Valor`.

Necesitarás elegir el campo de atributos que será utilizado en las etiquetas. En la lección anterior decidiste que el campo name era el más adecuado para tus objetivos.

* Selecciona `name` de la lista:

![Estilo de capas](/img/herramientaEtiquetado.png)

* Clic en Aplicar.

El mapa debería tener ahora etiquetas como estas:

![Etiquetas palces](/img/etiquetasPlaces.png)

### 4.2.2. Paso a Paso: Cambiando Opciones de Etiquetado

Dependiendo de los estilos que elegiste para tu mapa en las lecciones anteriores, puede que encuentres que las etiquetas no tienen el formato apropiado y se solapan o están demasiado lejos de sus puntos marcadores.

* Abre la herramienta `Opciones de etiquetado de capa` de nuevo haciendo clic en su botón como antes.
* Asegúrese de que `Texto` está seleccionado en la lista de opciones, después, actualice las opciones de formato de texto para que coincida con lo que se muestra aquí:

![Etiquetas palces texto](/img/etiquetasPlacesTexto.png)

¡El problema de fuente está resuelto! Ahora nos dirigimos al problema con las etiquetas solapadas con los puntos, pero antes de hacer esto, echemos un vistazo a la opción `Buffer`.

* Abre el cuadro de diálogo Herramienta de `Opciones de etiquetado de capa`.
* Selecciona `Buffer` de las opciones.
* Seleccione la casilla de verificación junto a `Dibujar buffer de texto`, después elija las opciones para que coincida con los que se muestran aquí:

![Etiquetas palces buffer](/img/etiquetasPlacesBuffer.png)

Verás que esto añade un un borde a las etiquetas de lugares, haciendo que sean fáciles de localizar en el mapa

Ahora podemos situar la posición de las etiquetas en relación con sus puntos marcadores.

* En el cuadro de diálogo Herramienta de `Opciones de etiquetado de capa`, ve a la pestaña `Ubicación`.
* Cambie el valor de Distancia a 2 mm y cerciórese que Alrededor del punto esté seleccionado.

![Etiquetas de places ubicación](/img/etiquetasPlacesUbicacion.png)

* Haz clic en Aplicar.

Verás que las etiquetas ya no se solapan con sus puntos marcadores.

### 4.2.3. Paso a Paso: Utilizando Etiquetas en lugar de Capas de Simbología

En muchos casos, la localización de un punto no necesita ser demasiado precisa. Por ejemplo, muchos de los puntos en la capa places se refieren a barrios, o áreas extensas, y el punto específico asociado a estas características no es tan preciso a gran escala. De hecho, dar un punto que es demasiado específico es a menudo confuso para el lector del mapa.

Para nombrar un ejemplo: en el mapa del mundo, un punto que represente la ubicación de Ecuador, podría estar en la provincia del Chimborazo. Para alguien leyendo el mapa sin conocer el país, ver un punto etiquetado como Ecuador en el Chimborazo, puede creer que la capital del país está en esa provincia.

Así, para prevenir este tipo de malentendidos, a menudo es útil desactivar los símbolos de punto y dejar visibles solamente las etiquetas.

En QGIS, también puedes hacerlo cambiando la posición de las etiquetas para representarlas directamente encima de los puntos a los que se refieren.

Abre el cuadro de diálogo Configuración de etiquetas de capa para la capa places.
Selecciona la opción Ubicación de la lista de opciones.
Haz clic en el botón Desplazamiento desde el punto.

Esto revelara las opciones Cuadrante que puedes utilizar para ajustar la posición de las etiquetas en relación con el punto marcador. En este caso, queremos centrar la etiqueta en el punto, así que elegiremos centrar cuadrante:

* Abre el cuadro de diálogo `Opciones de etiquetado de capa` de capa para la capa places.
* Selecciona la opción `Ubicación` de la lista de opciones.
* Haz clic en el botón `Desplazamiento desde el punto`.

Esto revelara las opciones Cuadrante que puedes utilizar para ajustar la posición de las etiquetas en relación con el punto marcador. En este caso, queremos centrar la etiqueta en el punto, así que elegiremos centrar cuadrante:

![Etiquetas de places ubicación](/img/etiquetasPlacesUbicacionDesplazamiento.png) 

* Oculta los símbolos de punto desde la pestaña `Estilo`  y `Aplicar`. 

![Etiquetas de places ubicación no sim](/img/etiquetasPlacesUbicacionDesplazamientoNoSim.png) 

### 4.2.4. :pencil2: Inténtalo tú! Personalizar las Etiquetas



### 4.2.5. Paso a Paso: Etiquetando Líneas
### 4.2.6. Paso a Paso: Ajustes Definidos de Datos
### 4.2.7. :pencil2: Inténtalo tú! Utilizando Ajustes Definidos de Datos
### 4.2.8. Más Posibilidades Con Etiquetas
### 4.2.9. En Conclusión
### 4.2.10. ¿Qué sigue a continuación?
## 4.3 Lección: Clasificación
### 4.3.1. Paso a Paso: Clasificación de Datos Nominales
### 4.3.2. :pencil2: Inténtalo tú! Más Clasificación
### 4.3.3. Paso a Paso: Clasificación por Ratios
### 4.3.4. :pencil2: Inténtalo tú! Refinar la Clasificación
### 4.3.5. Paso a Paso: Clasificación basada en Reglas
### 4.3.6. En Conclusión
### 4.3.7. ¿Qué sigue a continuación?

