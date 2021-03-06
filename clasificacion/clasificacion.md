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

![Estilo de capas](/img/estiloDeCapas.png)

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
* Cambie el valor de `Distancia` a 2 mm y cerciórese que `Alrededor del punto` esté seleccionado.

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

* Vuelve a los ajustes de etiqueta y símbolos que tenías anteriormente para tener un punto marcador y una etiqueta separados por 2.00mm. Puede que quieras ajustar el estilo del punto marcador o de las etiquetas en este punto.

> Su mapa ahora debe presentar los puntos del marcador y las etiquetas deben compensarse por 2.0 mm: El estilo de los marcadores y etiquetas debe permitir que sean claramente visibles en el mapa

* Ajusta el mapa a escala 1:50000. Puedes hacerlo escribiéndolo en la caja `Escala` en la `Barra de estado`.
* Modifica tus etiquetas para adecuarlas a la vista en esa escala.

### 4.2.5. Paso a Paso: Etiquetando Líneas

Ahora que sabes cómo funcionan las etiquetas, hay un problema adicional. Los puntos y polígonos son fáciles de etiquetar, pero ¿Qué pasa con las líneas? Si las etiquetas del mismo modo que los puntos, el resultado se verá así:

![Etiquetas lineas muy basico](/img/etiquetasLineasMuyBasico.png) 

Ahora daremos un nuevo formato a las etiquetas de la capa roads para que sean fáciles de entender.

* Oculta la capa `Places` para que no te moleste.
* Activa las etiquetas de la capa `roads` como antes.
* Ajusta el `Tamaño` de fuente a 10 para poder ver más etiquetas.
* Amplía el zoom al área central de la ciudad

Probablemente encontrarás el estilo de texto con valores por defecto y las etiquetas resultarán difíciles de leer. Ajusta el formato de texto de las etiquetas a un `Color` gris oscuro o negro y un `Buffer` amarillo pálido.

El mapa se verá parecido a esto, dependiendo de la escala:

![Etiquetas lineas muy basico con buffer](/img/etiquetasLinesConBuffer.png) 

Verás que algunos de los nombres de las calles aparecen más de una vez y que no siempre son necesarios. Para prevenir esto:

En el cuadro de diálogo `Configuración del etiquetado de la capa`, elige la opción `Representación`y selecciona `Combinar líneas combinadas para evitar etiquetas duplicadas`:

![Etiquetas lineas representacion](/img/etiquetasLineasRepresentacion.png) 

* Clic en `Aplicar`

Otra función útil es prevenir que las etiquetas se dibujen con caracteres demasiado pequeños para ser apreciados.

* En el mismo panel `Representación`, ajusta el valor de `Suprimir etiquetado de objetos espaciales menores que` a 5mm y nota los resultados cuando hagas clic en `Aplicar`.

Prueba diferentes ajustes de `Ubicación`. Como hemos visto anteriormente, la opción `Paralelo` no es una buena idea en este caso, así que prueba mejor con `Curvo`.

* Selecciona la opción `Curvo` en el panel `Ubicación` del cuadro de diálogo `Opciones de etiquetado de capa`.

Aquí está el resultado:

  

### 4.2.6. Paso a Paso: Ajustes Definidos de Datos

* Desactiva las etiquetas de la capa `roads`.
* Reactiva las etiquetas para la capa `places`.
* Abre la tabla de atributos para `places` a través del botón ![Boton tabla atributos](/img/botonTablaAtributos.png).

Tiene un campo que nos interesa ahora: `place` que define el tipo de área urbana para cada objeto. Podemos usar estos datos para influir en los estilos de las etiquetas.

* Navega al panel `Texto` en el panel `Etiquetas`.
* En el menú desplegable `Cursiva` (Marcado con una C o una I) selecciona Editar...  para abrir Etiqueta basada en expresión:

![Editar estilo](/img/etiquetaEditar.png).

En el cuadro de texto, escribe ```“place” = 'village'``` y clic Aceptar:

![Editar estilo village](/img/etiquetaEditarVillage.png)

> Nota los efectos: Verás que los `places` igual al `village` ahora tienen letra cursiva.

### 4.2.7. :pencil2: Inténtalo tú! Utilizando Ajustes Definidos de Datos

> Nota: Estamos saltando hacia adelante un poco para demostrar algunos ajustes avanzados de las etiquetas. En el nivel avanzado, se asume que sabrás qué significa lo siguiente. En caso contrario, eres libre de dejar esta sección y volver cuando hayas cubierto los materiales requeridos.

* Abre la Tabla de Atributos para `places`.
* Entra en el modo editar haciendo clic en el botón: ![Editar atributos](/img/editar.png)
* Abre la `Calculadora de campos`: ![Calculadora de campos](/img/calculadoraCampos.png)

Configúrala como ésta:

```
CASE 
WHEN "place" IS 'city' THEN 16 
WHEN "place" IS 'neighbourhood' THEN 14
WHEN "place" IS 'village' THEN 12
WHEN "place" IS 'square' THEN 10
ELSE 8
END
```

![Calculadora de campos font size](/img/fontSize.png)

* Asegúrate de guardar los cambios realizados en la tabla de atributos: ![Guardar edit](/img/guardarEdicion.png)
* Utiliza esto para ajustar y personalizar los tamaños de fuente para cada tipo de sitio distinto.

![Cambiar tamaño de fuente](/img/editarFontSize.png)

Deberás ver como tamaño de fuente cambia para cada tipo de `place`

### 4.2.8. Más Posibilidades Con Etiquetas

No podemos cubrir todas las opciones en este curso, pero date cuenta de que el Herramienta de `Opciones de etiquetado de capa` tiene muchas otras funciones útiles. Puedes ajustar representación basada en escala, alterar las prioridades de representación para las etiquetas en una capa, y ajustar cada opción de etiquetas utilizando la capa de atributos. Puedes incluso ajustar la rotación, posición XY, y otras propiedades de una capa (si tienes diferentes campos de atributos situados para tal fin). Puedes entonces editar las propiedades utilizando las herramientas adyacentes a la Herramienta de `Opciones de etiquetado de capa` principal. Estas herramientas estarán activas solamente si los campos de atributo requeridos están disponibles y el modo edición está activado.

![Herramientas De Etiquetas](/img/herramientasDeEtiquetas.png)herramientasDeEtiquetas

Si deseas aprender cómo funcionan estas opciones avanzadas de etiquetado, puedes consultar el manual de QGIS o buscar en internet ejemplos de [“Cómo mover etiquetas en QGIS”](https://gis.stackexchange.com/questions/183049/move-label-in-qgis).

Eres libre de explorar más posibilidades del sistema de etiquetas.

### 4.2.9. En Conclusión

Has aprendido a usar la capa de atributos para crear etiquetas dinámicas. Esto puede hacer tu mapa mucho más informativo y estilizado.

### 4.2.10. ¿Qué sigue a continuación?

Ahora que sabes cómo los atributos conllevan una diferencia visual en tu mapa, ¿Cómo los usamos para cambiar la simbología de los objetos? ¡Ese es el tema de la siguiente lección!

## 4.3 Lección: Clasificación

Las etiquetas son una buena forma de comunicar información como nombres de sitios individuales, pero no pueden ser usados para todo. Por ejemplo, supongamos que alguien quiere saber qué es cada uso de suelo `landuse`. Utilizando etiquetas, obtendrías esto:

![Clasificacion Landuse](/img/clasificacionLanduseEtiquetas.png)

Esto dificulta la lectura el etiquetado del mapa e incluso sería abrumador si hay muchos usos diferentes del territorio en un mapa.

**El objetivo de esta lección**: Aprender cómo clasificar los datos vectoriales efectivamente.

### 4.3.1. Paso a Paso: Clasificación de Datos Nominales

* Abrir el cuadro de diálogo `Propiedades de la Capa` para la capa `landuse`.
* Ir a la pestaña `Simbología`.
* Haga clic sobre la lista desplegable que dice `Símbolo único` y cambiarlo a `Categorizado`.
* En el nuevo panel, cambiar `Valor por landuse` y `Rampa de color` por `Greens`.
* Clic el botón  `Clasificar`:

![Clasificacion Landuse Categoriazado](/img/clasificacionLanduseCategorias.png)

* Clic en `Aceptar`

![Landuse Categoriazdo](/img/landuseClasificado.png)

Ahora nuestros polígonos de usos del territorio están correctamente coloreados y clasificados estando las áreas con el mismo uso del territorio del mismo color. Puede que quieras quitar el borde negro de la capa `landuse`:

* Abre `Propiedades de la capa`, ve a la pestaña `Simbología` y selecciona `Símbolo`.
* Cambia el símbolo eligiendo `Sin plumilla` en el `Estilo de marca` de la capa de símbolo `Relleno sencillo` y clic en `Aceptar`.

Verás que los contornos del polígono de usos del territorio se ha borrado, dejando solo nuestro relleno de colores para cada clasificación.

Si quieres, puedes cambiar el color de relleno para cada área de uso del territorio con doble clic en el bloque de color correspondiente.

![Landuse Categoriazdo Un Color](/img/landuseCambiarUnColor.png)

Nota que hay una categoría *`All other values`* que pertenecen a los valores vacíos.

La categoría vacía se usa para colorear cualquier objeto que no tenga un valor definido para uso del territorio o que tiene un valor NULL. Es importante mantener esta categoría para que las áreas con un valor NULL sigan representadas en el mapa. Puede que quieras cambiar el color a uno que represente mejor el valor en blanco o NULL.

¡Recuerda guardar tu mapa ahora para no perder todos tus laboriosos cambios!

### 4.3.2. :pencil2: Inténtalo tú! Más Clasificación

Si solo estás siguiendo el contenido del nivel básico, usa el conocimiento que has ganado anteriormente para clasificar la capa `buildings`. Ajusta la categorización en la columna de `buildings` y usa la rampa de color `Spectral`.

> Nota: Recuerda ampliar en un área urbana para ver los resultados.

### 4.3.3. Paso a Paso: Clasificación por Ratios

Hay cuatro tipos de clasificación: nominal, ordinal, de intervalos y relativa.

En clasificación **nominal**, las categorías en las que los objetos están clasificados están basadas en nombres; no tienen orden. Por ejemplo; nombres de ciudades, códigos postales, etc.

En clasificación **ordinal**, las categorías están organizadas en cierto orden. Por ejemplo, ciudades del mundo pueden tener un rango dependiendo de la importancia: Capital de País, Capital de Provincia, Capital de Cantón, etc.

En clasificación de **intervalos**, los números están en una escala con valores positivos, negativos y nulos. Por ejemplo: altura sobre/bajo el nivel del mar, temperatura sobre/bajo congelación (0 grados Centígrados), etc.

En clasificación por **razones**, los números están en una escala con sólo valores positivos y nulos. Por ejemplo: temperatura sobre cero absoluto (0 grados Kelvin), distancia desde un punto, cantidad media mensual de tráfico en una calle dada, etc.

En el ejemplo anterior, usamos clasificación **nominal** para representar cada tipo de uso del suelo. Ahora usaremos clasificación de rango para clasificar los usos del suelo por área.

* Guarda tu simbología de usos del suelo (si quieres conservarla) con clic en el botón `Guardar estilo` del cuadro de diálogo `Estilo`.

Vamos a reclasificar la capa, así que las clases existentes se perderán si no están guardadas.

* Cierra el cuadro de diálogo Estilo.
* Abre la `Tabla de Atributos` para la capa `landuse`.

Queremos clasificar las áreas de usos del suelo por tamaño, pero hay un problema: no tienen un campo de tamaño, así que tendremos que crearlo y calcularlo.

* Abre la Tabla de Atributos para `landuse`.
* Entra en el modo editar haciendo clic en el botón: ![Editar atributos](/img/editar.png)
* Abre la `Calculadora de campos`: ![Calculadora de campos](/img/calculadoraCampos.png)

Configúrala como ésta:

```
$area
```

* En la Lista de funciones, selecciona Geometría ‣ $area.

![Calculadora de campos area](/img/calcularArea.png)

* Asegúrate de guardar los cambios realizados en la tabla de atributos: ![Guardar edit](/img/guardarEdicion.png)
* Haz doble clic en ella para que aparezca en el campo `Expresión`
* Clic `Aceptar`.

Ahora tu campo AREA está lleno de valores.

> Nota: Debido a que el Sistema de Referencia de Coordenadas (SRC) es EPSG:4326 - WGS 84 - Geográfico, esas áreas están en grados. Luego los calcularemos en metros cuadrados.

* Abre la pestaña `Simbología` del cuadro de diálogo `Propiedades de la capa`.
* Cambia la clasificación del estilo de `Categorizado` a `Graduado`.
* Cambia el `Valor` a `area`:
* En `Rampa de color`, elige la opción `Crear nueva rampa de color...` para obtener este cuadro de diálogo:

![Nueva rampa de color](/img/nuevaRampaColor.png)

* Elige `Gradiente` (si no estaba ya seleccionada) y clic en `Aceptar`. Verás esto:

![Dialogo nueva rampa de color](/img/dialogoNuevaRampaColor.png)

Estarás usando esto para denotar áreas, con áreas pequeñas como `Color 1` y áreas grandes como `Color 2`.

* Elige los colores apropiados.

En el ejemplo, el resultado se ve así:

![Dialogo nueva rampa de color dos colores](/img/dialogoNuevaRampaColorEditado.png)

* Clic `Aceptar`.

Ahora tendrás algo como esto:

![Dialogo nueva rampa de color dos colores graduada](/img/clasificacionGraduada.png)

Deja todo lo demás como está.

* Clic en Aceptar:

![Mapa nueva rampa de color dos colores graduada](/img/mapaClasificacionGraduada.png)

### 4.3.4. :pencil2: Inténtalo tú! Refinar la Clasificación

* Quita las líneas de borde de los polígonos de uso del suelo.
* Cambia los valores de Modo y Clases hasta que obtengas una clasificación coherente.

> Usa el nombre del método como en el primer ejercicio de la lección para deshacerse de los límites
> Cambia `Clases` = 6 y `Modo` = `Rupturas Naturales(Jenks)` (y usando los mismos colores, por supuesto). Nota los cambios.

### 4.3.5. Paso a Paso: Clasificación basada en Reglas

Es común combinar múltiples criterios para una clasificación, pero desafortunadamente la clasificación normal solo tiene en cuenta un atributo. Ahí es donde la clasificación basada en reglas entra en juego.

* Abrir el cuadro de diálogo `Propiedades de la Capa` para la capa `landuse`.
* Escoge la pestaña `Simbología`.
* Ve al estilo de clasificación `Basado en reglas`. Tendrás esto:

![Clasificacion basado en reglas](/img/clasificacionReglas.png)

* Haga clic en el botón `Añadir regla` ![Anadir regla](/img/anadir.png).
* Un nuevo cuadro de diálogo aparecerá. En el campo `“Etiqueta”` coloca el nombre que aparecerá en la categoría, en este caso “Residencial”.
* Haz clic en el botón ![Expresion](/img/expresion.png) al lado del área de texto `Filtro`.
* Utilizando el constructor de consultas que aparece, escribe `"landuse" = 'residential'`, clic `Aceptar` y elige como color un naranja pálido y quita el borde.
* Añade una nueva nueva regla, ahora llamada `“Áreas verdes”`, y como filtro colocar   `"landuse"  =  'grass' OR  "landuse"  =  'forest' OR  "landuse"  =  'recreation_ground'`. Elige un color verde intermedio para el relleno y sin borde o estilo de marca.
* Añade un nueva nueva regla, ahora llamada `“Industrial”`, con el filtro `"landuse"  =  'industrial'` y asigna un color rosa.
* Finalmente añade una última regla, con el nombre `“Comercial”`, color café y el siguiente filtro:  `("landuse"   =  'commercial' OR  "landuse"   =  'retail' ) AND  "area" > 5000`

Las reglas que acabas de definir, asignan simbologías específicas de acuerdo a los atributos de cada elemento, de forma individual o combinada. Aquellos elementos que no coincidan con ninguna regla tomarán la simbología de la categoría `“(no filter)”`, por lo que podríamos asignar un color pálido más neutro. 

Tu cuadro de diálogo ahora ha quedado así:

![Reglas configuradas](/img/reglasConfiguradas.png)

Tu mapa se parecerá a este:

![Mapa reglas configuradas](/img/mapaReglas.png)

Ahora tienes un mapa con diferentes usos del suelo representados de diferentes maneras.

### 4.3.6. En Conclusión

La simbología nos permite representar los atributos de una capa de una forma sencilla de entender. También permite a los que visualicen el mapa entender el significado de las características, utilizando atributos relevantes que hemos escogido. Dependiendo del problema al que te enfrentes, aplicarás diferentes técnicas de clasificación para resolverlos.

### 4.3.7. ¿Qué sigue a continuación?

Ahora tenemos un bonito mapa, pero ¿Cómo obtendremos del QGIS un formato que se pueda imprimir o convertirlo en una imagen o PDF? ¡Ese es el tema de la siguiente lección!

