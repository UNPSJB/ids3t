.. include:: global.rst

.. _requerimientos no funcionales:

*****************************
Requerimientos no funcionales
*****************************

Introducción
============
Esta sección es una guía para la correcta gestión de los requerimientos no funcionales.

Alcance
=======

Los requerimientos no funcionales  se refieren a todos los requerimientos que no describen información a guardar, ni funciones a realizar, sino características de funcionamiento.

Requerimientos No Funcionales
=============================

Los requerimientos no funcionales describen lo bien que un sistema realiza su función, a diferencia de los requerimientos funcionales que son aquellos que describen el funcionamiento de dicho sistema.

Generalidades
=============

Debe pensarse en estos requerimientos como aquellas características que hacen al producto atractivo, usable, rápido y confiable.
Se conocen como un conjunto de características de calidad, que es necesario tener en cuenta al diseñar e implementar el Software.
No son parte de la razón fundamental del producto pero si son necesarios para hacer funcionar el producto de la manera deseada.
No modifican la funcionalidad del producto y si añaden funcionalidad al producto.

Categorías
==========

Existen diferentes categorías en los requerimientos no funcionales, a saber:

* Requerimientos de Apariencia.

* De Usabilidad.

* De Rendimiento.

* De Mantenibilidad y Portabilidad.

* De Seguridad.

* Legales.

Además existen otros menos usados pero igual de importantes:

* De Interfaz.

* De Desempeño.

* Operacionales y Económicos.

* Funcionalidad.

* Eficiencia y Simplicidad.

A continuación se describen las principales características no funcionales que debe contener un sistema.

**Interfaces de Usuario**: Los formularios y demás herramientas de apoyo deben ser intuitivos al usuario, debe existir la posibilidad de solicitar ayuda, su despliegue frente al usuario debe ser rápido, en el caso que sea una aplicación web debe permitir su navegación a través de los navegadores más comunes como Mozilla Firefox, Google Chrome e Internet Explorer y en las diferentes plataformas (Windows, Mac, Linux), deber ser autoajustable a cualquier tamaño y resolución de pantalla del usuario, debe utilizar imágenes optimizadas y componentes de diseño que permitan mostrar la información de manera dinámica, ágil y estética. 

Se debe considerar el diseño de interfaces para dispositivos móviles (celulares, tablets, etc.). 

**Requerimientos de desempeño**: Los tiempos de respuesta relacionados con formularios de manejo de información, adición, modificación, eliminación, consulta de registros, autenticación y emisión de avisos y confirmaciones por parte del usuario, en forma general, no deben ser superiores a 2.5 segundos, los informes y consultas que presenten una complejidad mediana no deben exceder el tiempo de 4 segundos. 

**Integridad**: El modelo de seguridad debe estar presente en cada una de las capas del sistema, garantizando el acceso autorizado a la información. No deben existir “puertas traseras” que permitan el manejo de información fuera del flujo lógico del sistema. Se requiere la encriptación de los principales datos almacenados en la base de datos. De igual forma se debe proveer un mecanismo de aseguramiento de integridad de toda la información registrada en la base de datos. Esta integridad, debe ser estructural y referencial.

**Control de Acceso Externo**: Se debe considerar que parte de la infraestructura presenta un esquema basado en redes seguras en donde se dispone de Firewalls mediante los cuales el manejo de puertos y protocolos son administrados desde este punto, y no desde los sistemas de información. 

Se debe considerar aspectos de seguridad relacionados a su utilización a través de redes públicas, garantizando la confidencialidad e integridad de la información y acceso a ella. 

**Auditoría**: Se debe implementar el registro de acciones realizadas por los usuarios a las principales transacciones (usuario, fecha, hora) y registros del sistema en lo relacionado con la creación, modificación y eliminación. 

**Flexibilidad**: La configuración de los parámetros de instalación no debe requerir modificaciones al código fuente de la instalación.

Debe ser totalmente independiente de la topología de red utilizada, es decir, el sistema debe poder funcionar en múltiples esquemas de comunicación, tanto para equipos conectados remotamente, como para equipos conectados por una red LAN, WAN o Internet y todas las combinaciones anteriormente descritas. 

**Disponibilidad**: El sistema no debe presentar ningún punto de fallo, es decir, debe estar provisto de mecanismos o componentes que aseguren la continuidad del servicio.

