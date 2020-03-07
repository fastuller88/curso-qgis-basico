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
    * [¿Qué sigue a continuación?](#que-sigue-a-continuacion)
* [Simbología](#simbologia)
    * [Paso a Paso: Cambiando colores](#paso-a-paso-cambiando-colores)
    * [Inténtalo tú!](#intentalo-tu)
    * [Paso a Paso: Cambiando la estructura del símbolo](#paso-a-paso-cambiando-la-estructura-del-simbolo)
    * [Inténtalo tú!](#intentalo-tu)
    * [Paso a Paso: Visibilidad Basada en Escala](#paso-a-paso-visibilidad-basada-en-escala)
    * [Paso a Paso: Añadiendo Capas de Símbolos](#paso-a-paso-anadiendo-capas-de-simbolos)
    * [Inténtalo tú!](#intentalo-tu)
    * [Paso a Paso: Ordenando los Niveles de Símbolos](#paso-a-paso-ordenando-los-niveles-de-simbolos)
    * [Inténtalo tú!](#intentalo-tu)
    * [Inténtalo tú!](#intentalo-tu)
    * [Paso a Paso: Tipos de Capas de Símbolos](#paso-a-paso-tipos-de-capas-de-simbolos)
        * [Tipos de Capas de Símbolos para Puntos](#tipos-de-capas-de-simbolos-para-puntos)
        * [Tipos de Capas de Símbolos para Líneas](#tipos-de-capas-de-simbolos-para-lineas)
        * [Tipos de Capas de Símbolos para Polígonos](#tipos-de-capas-de-simbolos-para-poligonos)
    * [(OPCIONAL) Paso a Paso: Creando un Relleno SVG Personalizado](#opcional-paso-a-paso-creando-un-relleno-svg-personalizado)
    * [En Conclusión](#en-conclusion)
    * [Más lecturas…](#mas-lecturas)
* [Estado de las capas](#estado-de-las-capas)
    * [Capas visibles](#capas-visibles)
    * [Capas activas](#capas-activas)
    * [Inténtalo tú! Mostrar, ocultar y activar capas.](#intentalo-tu-mostrar-ocultar-y-activar-capas)
    * [¿Qué sigue a continuación?](#que-sigue-a-continuacion)


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

Por ejemplo, en la carpeta `epsg4326/` hay varias capas: “places”, “rivers”, “roads”, etc. Cada una de esas capas está compuesta de varios archivos: ej: roads.dbf, roads.prj, roads.shp, etc… Es importante saber que todos los archivos son necesarios para abrir la capa, por lo que si quieres copiar una capa a otra carpeta o computadora, es necesario copiar todos los archivos que tengan el mismo nombre.

![Archivos shape](/img/archivosShape.png)

Los Archivos Shape son bastante comunes pero son anticuados y en varios casos difíciles de manejar, por lo que en la actualidad se suelen trabajar con otros tipos de archivos, tales como conjuntos de datos **spatialite**, **bases de datos**, o **geopackage**. 

Si no sabes como añadir una capa vectorial, regresa al [ejercicio introductorio](/interfaz/interfaz.md#anadiendo-tu-primera-capa).
Carga las siguientes capas desde la carpeta `epsg4326/` en su mapa siguiendo el mismo método:

“places”
“water”
“rivers”
“buildings”

### Paso a Paso: Cargando Datos Vectoriales desde un Conjunto de Datos Spatialite

A diferencia de los archivos shapefile, los **conjuntos de datos** te permiten guardar un gran volumen de datos asociados en un archivo. Puede que te resulte familiar un sistema de manejo de base de datos (DBMS) como Microsoft Access. Las aplicaciones SIG pueden también utilizar conjuntos de datos. SIG-específicos DBMS (como PostGIS) tienen funciones extra, ya que necesitan manejar datos espaciales. Uno de los formatos comunes de bases de datos espaciales es Spatialite, basado en el sistema de bases de datos sqlite.

* Haga clic en el administrador de fuentes de datos




