# La interfaz de QGIS
En esta sección te familiarizaras con la interfaz que nos presenta QGIS. Después de completar ésta sección, serás capaz de identificar correctamente los elementos básicos de la pantalla de QGIS y sabrás qué hace cada uno, y cargar un shapefile dentro de QGIS.

> Advertencia: Este curso incluye instrucciones para añadir, borrar y alterar bases de datos del SIG. Hemos proporcionado bases de datos de entrenamiento para éste propósito. Antes de usar técnicas descritas aquí en tus propios datos, siempre asegúrate de que tienes los backups adecuados!


## Contenidos

* [¿Por qué QGIS?](#por-qué-qgis)
* [Añadiendo tu primera capa](#añadiendo-tu-primera-capa)

## ¿Por qué QGIS?
Como la información se vuelve cada vez más espacialmente consciente, no hay escasez de herramientas capaces de satisfacer algunas o incluso todas las funciones utilizadas en SIG. ¿Por qué debería uno utilizar QGIS en lugar de otros paquetes de software de GIS?.

Aquí hay solo algunas de las razones:

* **Es gratis**. Instalando y utilizando QGIS te cuesta la total cantidad de cero dinero. Sin cuota inicial, ni cargo fijo, nada.
* **Es libre**. Si necesitas más funciones en QGIS, puedes hacer más que esperar a que sean incluidas en la siguiente versión. Puedes patrocinar el desarrollo de la función, o añadirla tú mismo si estás familiarizado con programación.
* **Está en constante desarrollo**. Porque cualquiera puede añadir nuevas funciones y mejorar las ya existentes, QGIS nunca se estanca. El desarrollo de una nueva herramienta puede ocurrir tan rápidamente como tu lo necesitas.
* **Extensa ayuda y documentación está disponible**. Si te estancas con cualquier cosa, puedes ayudarte con la extensa documentación, tus compañeros de QGIS, o incluso en los promotores.
* **Multiplataforma**. QGIS puede ser instalado en MacOS, Windows y Linux.

## Añadiendo tu primera capa 

> Nota: Antes de comenzar este ejercicio, QGIS debe estar instalado en su computadora.

Descarga el archivo comprimido con los datos para éste curso haciendo click en el siguiente enlace: [trainingdata_QGIS_cuenca](https://github.com/fastuller88/curso-qgis-basico/raw/master/data/trainingdata_QGIS_cuenca.zip). Debes descomprimir el archivo en una carpeta en tu disco duro antes de comenzar a trabajar.

> Nota: Las capturas de pantalla para este curso se tomaron utilizando  QGIS 3.10. Dependiendo de tu instalación, las pantallas que encontrarás puede que sean algo diferentes. Sin embargo, los mismos botones estarán disponibles, y las instrucciones funcionarán en cualquier SO. Necesitarás QGIS 3.10 (la versión más reciente al momento de la escritura) para usar este curso. Si algo no corresponde a lo que aparece en el programa, puede ser que aún el manual no esté actualizado. Por favor contactar al autor: johnatan.astudillo@gmail.com para solicitar la correspondiente actualización del material.

### Paso a paso: Prepara un mapa

* Abre QGIS. Tendrás un nuevo mapa en blanco.
* Busca el botón `Administrador de fuente de datos`: ![Añadir capa](img/addLayer.png) y haz click en él para abrir el siguiente diálogo:
![Dialogo administrador fuente de datos](img/fuenteDeDatos.png)
* Clica en el botón de explorar ![Explorar](img/explorar.png) y navega al archivo `trainingdata_QGIS/epsg4326WGS84/roads.gpkg` (en el directorio de tu curso). Con este archivo seleccionado, clica en `Abrir`. Verás el diálogo original, pero con la ruta de archivo rellena. Clica en `Añadir`. Los datos que has especificado se cargarán.

¡Enhorabuena! :+1:  Ya tienes un nuevo mapa básico. Ahora sería un buen momento para guardar tu trabajo.

* Haga clic en el botón `Guardar Proyecto`...:![Guardar Proyecto](img/guardar.png)
* Guarda el mapa en `exercise_data/` y nómbralo `mi_primer_mapa.qgz`.

## Una vista general de la interfaz

Exploraremos la interfaz de usuario de QGIS, de forma que se familiarice con los menús, barras de herramientas, lienzo del mapa y lista de capas, que forman la estructura básica de la interfaz.
![Vista General](img/vistaGeneral.png)

Los elementos identificados en la figura superior son:

* :one: Panel de capas
* :two: Panel del explorador
* :three: Barras de herramientas
* :four: Lienzo del mapa
* :five: Barra de estado

Abre un proyecto e identifica los elementos

* Busca el botón `Abrir proyecto`: ![Abrir proyecto](img/abrir.png) 
* Navega al archivo `trainingdata_QGIS/proyectos/general.qgz` (en el directorio de tu curso). Clica en `Abrir`. Los datos que has especificado se cargarán.

:eyes: [Comprueba tus resultados](/respuestas/respuestas.md#resultados-para-añadiendo-tu-primera-capa)

### :one: Panel de capas  

En el panel de capas puede ver una lista, en cualquier momento, de todas las capas que están disponibles.
En la parte superior del panel están  herramientas que le permitirá administrar las capas mediante la creación de grupos, eliminación de capas,  leyendas, visibilidad de capas, expansión de los contenidos de cada capa y el estilo de capa.

Expandiendo los elementos colapsados (haciendo clic en la flecha o símbolo más a su lado) se obtiene más información sobre el aspecto actual de la capa.
Un clic derecho sobre una capa mostrará un menú con muchas opciones extra. ¡Pronto estará usando algunas de ellas, así que écheles un vistazo!

### :two: Panel del explorador  

El explorador de QGIS es un panel que le permite navegar fácilmente por las carpetas de su computadora o sus base de datos. Puede acceder desde este panel a archivos vectoriales comunes (ej. archivos shape de ESRI o GeoPackge), bases de datos (ej. PostGIS, Oracle, Spatialite o MYSQL Spatial) y conexiones WMS/WFS. Generalmente este panel puede no aparecer por defecto, pero podemos agregarlo a nuestro ambiente de trabajo siguiendo las instrucciones del siguiente punto.

### :three: Barras de herramientas 

Sus conjuntos de herramientas más utilizadas se pueden convertir en barras de herramientas para un acceso más rápido. Por ejemplo, la `barra de herramientas del proyecto` le permite guardar, abrir, imprimir e iniciar un nuevo proyecto. Puede fácilmente personalizar la interfaz para ver sólo las herramientas que use más a menudo, añadiendo o eliminando barras de herramientas según necesite al hacer un clic derecho sobre la barra de menús se abrirá un cuadro de diálogo donde se listan `Herramientas / Paneles y Barras de herramientas`, basta con seleccionarlas para que aparezcan en el ambiente de trabajo.

Incluso si no son visibles en una barra de herramientas, todas sus herramientas están disponibles a través de los menús. Por ejemplo, si elimina la barra de herramientas la `barra de herramientas del proyecto` (que contiene el botón `Guardar`), aún podrá guardar su mapa al hacer clic en el menú `Proyecto` y luego en `Guardar`.

### :four: Lienzo del mapa 

Aquí es donde se muestra el mapa propiamente dicho.

### :five: Barra de estado 

Muestra información sobre el mapa actual. También le permite ajustar la escala del mapa y ver las coordenadas del cursor del ratón en el mapa.

### 









