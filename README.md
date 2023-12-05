# Exploración de los datos abiertos bases históricas de enfermedades transmitidas por vector de México

Este trabajo es el proyecto final de la materia de Introducción a la Ciencia de Datos, de la Maestría en Ciencia de Datos de la Universidad de Sonora. El ojetivo general del presente proyecto es aplicar algunas de las herramientas vistas durante el curso. De entre estas herramientas, se destaca la creación y manipulación de estructuras de datos en SQL. Esto se efectúa dentro de un entorno de programación Python, de modo que dichas manipulaciones puedan complementarse con visualizaciones de la relación entre variables.

**Integrantes de equipo**
- Barreras Maldonado José Carlos
- Gaytan Villareal Jesús Martin
- Merino Cedeño Angel Alberto
- Minjares Neriz Victor Manuel

## Datos utilizados

En este repositorio exploramos los casos de dengue en México, tanto a nivel federal como estatal. Los datos fueron obtenidos de
esta [página](https://www.gob.mx/salud/documentos/datos-abiertos-bases-historicas-de-enfermedades-transmitidas-por-vector) y son del año 2023,
hasta el día 26 de octubre. A continuación se presenta una tabla descriptiva con cada una de las variables que conforman nuestros datos.

| NO. | NOMBRE DE VARIABLE   | DESCRIPCIÓN                                                 | FORMATO O FUENTE                                       |
|-----|-----------------------|-------------------------------------------------------------|--------------------------------------------------------|
| 1   | FECHA_ACTUALIZACION   | LA BASE DE DATOS SE ACTUALIZA SEMANALMENTE. ESTA VARIABLE PERMITE IDENTIFICAR LA ÚLTIMA ACTUALIZACIÓN.          | AAAA-MM-DD, 9999-99-99: CUANDO NO HAY REGISTRO         |
| 2   | ID_REGISTRO           | NÚMERO DE IDENTIFICADOR DEL CASO                             | TEXTO                                                  |
| 3   | SEXO                  | IDENTIFICA EL SEXO DEL PACIENTE                               | CATÁLOGO: SEXO                                         |
| 4   | EDAD_ANOS             | IDENTIFICA LA EDAD EN AÑOS DEL PACIENTE                        | NÚMERICA EN AÑOS                                       |
| 5   | ENTIDAD_RES           | IDENTIFICA LA ENTIDAD DE RESIDENCIA DEL PACIENTE               | CATÁLOGO: ENTIDADES                                     |
| 6   | MUNICIPIO_RES         | IDENTIFICA EL MUNICIPIO DE RESIDENCIA DEL PACIENTE             | CATÁLOGO: MUNICIPIOS                                   |
| 7   | HABLA_LENGUA_INDIG    | IDENTIFICA SI EL PACIENTE HABLA LENGUA INDÍGENA                | CATÁLOGO: SI / NO                                      |
| 8   | INDIGENA              | IDENTIFICA SI EL PACIENTE SE AUTOIDENTIFICA COMO PERSONA INDÍGENA | CATÁLOGO: SI / NO                                    |
| 9   | ENTIDAD_UM_NOTIF      | IDENTIFICA LA ENTIDAD DONDE SE ENCUENTRA LA UNIDAD MÉDICA NOTIFICANTE | CATÁLOGO: ENTIDADES                                 |
| 10  | MUNICIPIO_UM_NOTIF    | IDENTIFICA EL MUNICIPIO DONDE SE ENCUENTRA LA UNIDAD MÉDICA NOTIFICANTE | CATÁLOGO: MUNICIPIOS                               |
| 11  | INSTITUCION_UM_NOTIF  | IDENTIFICA LA INSTITUCIÓN DE LA UNIDAD MÉDICA NOTIFICANTE      | CATÁLOGO: INSTITUCIÓN                               |
| 12  | FECHA_SIGN_SINTOMAS   | IDENTIFICA LA FECHA DE INICIO DE SIGNOS Y SÍNTOMAS DEL CUADRO CLÍNICO ACTUAL | AAAA-MM-DD, 9999-99-99: CUANDO NO HAY REGISTRO    |
| 13  | TIPO_PACIENTE         | IDENTIFICA EL TIPO DE ATENCIÓN QUE RECIBIÓ EL PACIENTE EN LA UNIDAD | CATÁLOGO: TIPO_PACIENTE                            |
| 14  | HEMORRAGICOS          | PRESENCIA DE TRASTORNOS HEMORRÁGICOS                           | CATÁLOGO: SI / NO                                      |
| 15  | DIABETES              | PRESENCIA DE DIABETES                                         | CATÁLOGO: SI / NO                                      |
| 16  | HIPERTENSION          | PRESENCIA DE HIPERTENSIÓN                                      | CATÁLOGO: SI / NO                                      |
| 17  | ENFERMEDAD ULC_PEPTICA | PRESENCIA DE ENFERMEDAD ÚLCERO PÉPTICA                         | CATÁLOGO: SI / NO                                      |
| 18  | ENFERMEDAD_RENAL       | PRESENCIA DE ENFERMEDAD RENAL                                   | CATÁLOGO: SI / NO                                      |
| 19  | INMUNOSUPR            | PRESENCIA DE INMUNOSUPRESIÓN                                   | CATÁLOGO: SI / NO                                      |
| 20  | CIRROSIS_HEPATICA      | PRESENCIA DE CIRROSIS HEPÁTICA                                 | CATÁLOGO: SI / NO                                      |
| 21  | EMBARAZO              | IDENTIFICA SI LA PACIENTE ESTÁ EMBARAZADA                      | CATÁLOGO: SI / NO                                      |
| 22  | DEFUNCION             | INDICA SI EL PACIENTE FALLECIÓ                                 | CATÁLOGO: SI / NO                                      |
| 23  | DICTAMEN              | IDENTIFICA EL RESULTADO DE LA DICTAMINACIÓN PARA EL PACIENTE   | CATÁLOGO: DICTAMEN                                     |
| 24  | TOMA_MUESTRA          | IDENTIFICA SI AL PACIENTE SE LE TOMÓ MUESTRA                   | CATÁLOGO: SI / NO                                      |
| 25  | RESULTADO PCR         | IDENTIFICA EL RESULTADO DE LA PRUEBA PCR REALIZADA POR EL LABORATORIO | CATÁLOGO: RESULTADO_PCR                            |
| 26  | ESTATUS_CASO          | ESTATUS DEL CASO                                              | CATÁLOGO: ESTATUS_CASO                                 |
| 27  | ENTIDAD_ASIG          | IDENTIFICA LA ENTIDAD A LA QUE SE ASIGNÓ EL CASO               | CATÁLOGO: ENTIDADES                                    |
| 28  | MUNICIPIO_ASIG        | IDENTIFICA EL MUNICIPIO AL QUE SE ASIGNÓ EL CASO               | CATÁLOGO: MUNICIPIOS                                   |

Junto con los datos, se descargaron también los catálogos para decodificar las variables categórico-numéricas.





