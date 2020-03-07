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
Los datos vectoriales son posiblemente el tipo más común de los datos que se encuentran en el uso diario de los SIG. En él se describen los datos geográficos en términos de puntos, que se puede conectar a las líneas y polígonos. Cada objeto en un conjunto de datos de vectores se llama una característica, y se asocia con los datos que describe esa característica.
El objetivo de esta lección. Aprender acerca de la estructura de los datos vectoriales, y cómo cargar un conjunto de datos vectoriales dentro de un mapa.

