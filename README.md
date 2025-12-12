# Gestión de incendios forestales en España

Este repositorio contiene el trabajo realizado para el análisis, modelado y visualización de incendios forestales en España, combinando técnicas de integración de datos, modelado dimensional y representación semántica mediante RDF.

## Descripción del proyecto

El objetivo del proyecto es analizar la evolución y el riesgo de los incendios forestales a nivel provincial en España, con el fin de obtener información útil para la prevención, la gestión del territorio y la toma de decisiones.

Para ello, se ha trabajado con datos oficiales del Ministerio para la Transición Ecológica (MITECO), que han sido limpiados, normalizados e integrados en un Data Warehouse. Posteriormente, los datos se han transformado a un modelo RDF siguiendo el vocabulario de schema.org, permitiendo representar los incendios como un grafo de conocimiento enlazado con Wikidata.

Finalmente, se han generado dos visualizaciones:
- Un ranking de provincias según el número total de incendios, a partir del RDF.
- Una evolución temporal del riesgo, calculado como incendios por superficie forestal, a partir de datos en CSV.

## Contenido del repositorio

- incendios.ttl  
  Archivo RDF en formato Turtle que contiene el grafo de conocimiento con los incendios (schema:Event) y las provincias (schema:Place), enlazadas mediante schema:location y enriquecidas con Wikidata.

- modelo_conceptual_incendios.png  
  Diagrama del diseño conceptual del Data Warehouse.

- modelo_logico_incendios.png  
  Esquema lógico en estrella utilizado para el análisis.

- modelo_fisico_incendios.sql  
  Script SQL con la definición de las tablas del modelo físico.

- transformacion_RDF_incendios.py  
  Código utilizado para la transformación del dataset limpio a RDF mediante la librería RDFlib.

- visualizaciones_incendios_*.py  
  Scripts utilizados para generar las visualizaciones del ranking y de la evolución temporal del riesgo.

- README.md  
  Descripción general del proyecto y del contenido del repositorio.

## Tecnologías utilizadas

- Python  
- RDFlib  
- SQL  
- Pentaho Data Integration  
- RDF / Turtle  
- schema.org  
- Wikidata  

## Licencia

Este proyecto se distribuye bajo la licencia MIT

## Autoras

- Claudia Fernández  
- Irene Alavés  
- Eva Graña
