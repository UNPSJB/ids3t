.. include:: global.rst

.. _configuracion:

***************************
Gestión de la Configuración
***************************

Introducción
============

Esta sección es una guía para la correcta gestión de la configuración del proceso de desarrollo. Incluye los lineamientos necesarios para el manejo de versiones de los diferentes componentes, el manejo de las diferentes ramas y responsabilidades y actividades de los distintos actores.

Alcance
=======

El plan de la Gestión de la Configuración

El plan de configuración está basado en algunos supuestos que se detallarán: 

* Tener control sobre cada una de las iteraciones y fases, de los productos generados  en estas y de los cambios surgidos, evaluados y aprobados. 
* Se deben incluir en control de configuración la mayor cantidad de productos posibles, tomando en cuenta siempre las restricciones dadas por la duración del  proyecto y por la capacidad organizativa del equipo. 
* Si es necesario, se realizarán las modificaciones que el cliente ha pedido y se  actuará con las estrategias pertinentes. 
* La elección de los elementos de configuración se realizará en base a los entregables, siendo esta responsabilidad del Responsable de SCM, apoyado por los integrantes de cada disciplina. 
* Al concluir cada una de las iteraciones, se llevará a cabo una prueba de verificación  de la funcionalidad.

Objetivos
=========

Los objetivos de la Gestión de la Configuración son:

    * Determinar cuál es la versión actual de cada uno de los componentes.
    * Determinar el proceso cambios.
    * Determinar la política de releases.

Roles y Responsabilidades
========================= 

+------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Roles                        | Responsabilidades                                                                                                                                                                               |
+==============================+=================================================================================================================================================================================================+
| Gestor de configuración      | - Gestionar la planificación, identificación, control, seguimiento y auditoría de todos los elementos de configuración en la base de datos de configuración.                                    |
|                              | - Desarrollar el plan de gestión de configuración.                                                                                                                                              |
|                              | - Promover el uso efectivo de la base de datos de configuración dentro de la organización.                                                                                                      | 
|                              | - Monitorear y reportar los cambios no autorizados sobre los elementos de configuración.                                                                                                        |
|                              | - Asegurar la consistencia e integridad de los datos de la base de datos de configuración a través de la ejecución de procedimientos de verificación y auditoría.                               | 
|                              | - Liderar las actividades de evaluación del proceso: revisar tipos de elementos de configuración, relaciones, atributos y valores asociados, estructura de la base de datos, derechos de acceso.| 
|                              | - Aprobar cambios estructurales en la base de datos de configuración.                                                                                                                           |
+------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Coordinador de configuración | - Asegurar que todos los elementos de configuración están registrados de forma adecuada en la base de datos de configuración.                                                                   |
|                              | - Asegurar la consistencia e integridad de los datos de la base de datos de configuración y la estructura del sistema a través de la ejecución de procedimientos de verificación y auditoría.   |
|                              | - Reportar cualquier discrepancia o no conformidad en los elementos de configuración al gestor de configuración.                                                                                |
|                              | - Participar en la mejora continua del proceso de gestión de configuración.                                                                                                                     |
+------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Responsable de elementos     | - Asegurar que los elementos de configuración de los que es responsable están registrados en la base de datos de configuración con el estado y datos de configuración apropiados.               |
| de configuración             | - Verificar que los cambios sobre los elementos de configuración siguen el proceso de cambios definido.                                                                                         |
|                              | - Asegurar la idoneidad e integridad de los elementos de configuración de los que es responsable.                                                                                               |
|                              | - Trabajar conjuntamente con el gestor de configuración para identificar las causas de cualquier discrepancia identificada en las auditorías e implementar las acciones correctivas.            |
+------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Gestor de cambio             | - Evaluar el impacto y riesgo de los cambios.                                                                                                                                                   |
|                              | - Asegurar que los responsables de los elementos de configuración actualizan los históricos de estos elementos con los cambios implementados.                                                   |
+------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Actividades de Gestión de Configuración
=======================================

En la siguiente tabla, se recogen de forma resumida las actividades que conforman el proceso de gestión de configuración.

+---------------------------------------------------------+--------------------------------------------+------------------------------------------------------------------------------------------------------+---------------------------------------------+--------------------------------------------+
| Actividad                                               | Rol Responsable                            | Descripción                                                                                          | Entradas                                    | Salidas                                    |
+=========================================================+============================================+======================================================================================================+=============================================+============================================+
| Gestión del proceso de gestión de configuración.        | Gestor de configuración.                   | Documentar el plan de gestión de configuración.                                                      | Necesidades del proyecto. Plan de proyecto. | Plan de gestión de configuración aprobado. |
+---------------------------------------------------------+--------------------------------------------+------------------------------------------------------------------------------------------------------+---------------------------------------------+--------------------------------------------+
| Identificación de elementos de configuración.           | Gestor de configuración.                   | Identificar elementos de configuración. Crear estructura del directorio de gestión de configuración. | Productos del proyecto.                     | Elementos de configuración identificados.  |
|                                                         |                                            |                                                                                                      |                                             | Línea base. Estructura del directorio de   |
|                                                         |                                            |                                                                                                      |                                             | gestión de configuración.                  |
+---------------------------------------------------------+--------------------------------------------+------------------------------------------------------------------------------------------------------+---------------------------------------------+--------------------------------------------+
| Mantenimiento y control de la gestión de configuración. | Responsable del elemento de configuración. | Control de cambios sobre elementos de configuración y líneas base. Obtener aprobación de solicitudes | Peticiones de cambio.                       | Registro de solicitud de cambio. Solicitud | 
|                                                         |                                            | de cambio sobre productos de trabajo de línea base.                                                  |                                             | de cambio aprobada. Línea base.            |
+---------------------------------------------------------+--------------------------------------------+------------------------------------------------------------------------------------------------------+---------------------------------------------+--------------------------------------------+
| Informe de estado de la configuración.                  | Gestor de configuración.                   | Mantener actualizado y publicar el estado de los elementos de configuración.                         | Elementos de configuración.                 | Informe de estado de elementos de          |
|                                                         |                                            |                                                                                                      |                                             | configuración.                             |
+---------------------------------------------------------+--------------------------------------------+------------------------------------------------------------------------------------------------------+---------------------------------------------+--------------------------------------------+
| Verificación y auditoría.                               | Gestor de configuración.                   | Realizar auditorías de la gestión de configuración.                                                  | Registros de la gestión de configuración.   | Informe de auditoría de gestión de         |
|                                                         |                                            |                                                                                                      | Línea base. Registros de cambios.           | configuración.                             |
+---------------------------------------------------------+--------------------------------------------+------------------------------------------------------------------------------------------------------+---------------------------------------------+--------------------------------------------+

Identificación de Elementos de Configuración
============================================

La actividad de identificación de la configuración identifica los elementos que van a ser controlados, establece esquemas para la identificación de los elementos y sus versiones, y establece las herramientas y técnicas a usar para adquirir y gestionar los elementos controlados. Estas actividades proporcionan la base para otras actividades de gestión de configuración. 
Las principales tareas a llevar a cabo dentro de esta actividad son: 

- Identificar los productos que se van a mantener bajo gestión de configuración para el proyecto.
- Asignar identificadores únicos para cada elemento de configuración y propiedades como autor, tipo de documento o fichero, persona responsable de ese elemento de configuración, etc. 
- Definir estructura de almacenamiento.
- Definir un nivel de control de acceso de los miembros del equipo sobre la infraestructura de almacenamiento.
- Seleccionar herramientas específicas para la gestión de configuración.
- Especificar cuándo se va a incluir cada elemento bajo gestión de configuración (en qué momento del ciclo de vida).
- Obtener la autorización para incluir los documentos bajo gestión de configuración (línea base).
- Aplicar los procedimientos definidos para incluir los productos bajo gestión de configuración.
- Documentar los elementos que se han incluido bajo gestión de configuración.
- Desarrollar procedimientos para solicitar e implantar los cambios donde se especifique:

    * Quién solicita los cambios
    * Cómo se notifican los cambios
    * Cómo se evalúa el impacto
    * Quién evalúa el impacto
    * Quién acepta o rechaza el cambio
    * Quién modifica los distintos productos (responsable de cada producto)

A la hora de seleccionar los elementos que estarán bajo gestión de configuración, se pueden tener en cuenta criterios como los siguientes:

- Productos de trabajo que vayan a ser utilizados por dos o más grupos.
- Productos de trabajo que puedan cambiar con el tiempo debido a cambios en requisitos o errores.
- Productos que dependan de otros en el sentido de que un cambio en uno de ellos implique un cambio en los otros.
- Productos de trabajo que sean críticos para el proyecto.

Dependiendo de la naturaleza del proyecto los elementos de configuración pueden variar de un proyecto a otro.
Elementos de configuración:

- Planes
    * Plan de proyecto
    * Plan de calidad
    * Plan de gestión de configuración
    * Plan de gestión de riesgos
    * …

- Registros del proyecto
- Material de apoyo al cliente
- Especificación de requisitos

    * Requisitos de negocio
    * Requisitos de usuario
    * Requisitos de sistema

- Matriz de trazabilidad de requisitos
- Documentos de diseño
- Resultados de la resolución y análisis de decisión
- Código fuente
- Plan de integración de software
- Informes resultantes de las revisiones realizadas en los puntos de comprobación o al final de las fases
- Plan de pruebas o unitarias o de integración o de sistemas o de aceptación de usuario o de regresión
- Datos de pruebas y casos de pruebas
- Plan de instalación/mantenimiento
- Documentos de manual de usuario
- Plan de entrega de servicios
- Informes de investigación
- Informes de estimación
- Informes de cierre del proyecto
- Prototipos
- Informes de métricas
- Todos los entregables enviados al cliente.

Mantenimiento y control de la gestión de la configuración
=========================================================

Cuando se solicita un cambio que afecta a algún producto bajo gestión de configuración (línea base), entrará en funcionamiento el proceso de control de cambios. En este proceso, que se explicará a continuación, se deben identificar y valorar los cambios y, si son admitidos, modificar los productos afectados, siguiendo el procedimiento establecido. Estos cambios realizados deben comunicarse a todas las personas que resulten afectadas por los mismos.

Proceso de control de cambios
=============================

Como primer paso para gestionar los cambios sobre los elementos controlados es determinar los cambios que se van a realizar. El proceso de petición de cambios proporciona procedimientos formales para enviar y registrar peticiones de cambio, evaluar el coste e impacto potencial del cambio propuesto, y aceptar, modificar, o rechazar el cambio propuesto.

Los cambios solicitados o los errores detectados deberán ser identificados a través de los canales preestablecidos (personas, herramientas, etc.). Una vez recibidos serán documentados para su posterior estudio.

Las peticiones de cambio sobre elementos de configuración pueden iniciarse por cualquiera y en cualquier punto del proceso de desarrollo y pueden incluir una sugerencia de solución y prioridad de la petición. Un posible origen de las peticiones de cambio es el inicio de una acción correctiva en respuesta a informes de problemas. El tipo de cambio (p.ej.: defecto o mejora) se debe registrar en la petición de cambio (SCR) para así poder recoger métricas sobre los cambios por tipo de cambio.

Una vez recibida una SCR, se realizará una evaluación técnica o análisis de impacto para determinar el alcance de las modificaciones que serían necesarias realizar una vez se acepte la petición. En este punto es importante un buen entendimiento de las relaciones entre los elementos de software. Según la línea base afectada, los elementos de configuración implicados, y la naturaleza del cambio, la persona responsable deberá evaluar los aspectos técnicos y de gestión de la petición de cambio, y a continuación aceptar, modificar, rechazar o aplazar el cambio propuesto. En cualquier caso, la decisión tomada deberá quedar documentada de alguna forma.

Las SCR aprobadas se implementarán utilizando los procedimientos de software definidos de acuerdo a los requisitos de tiempo que apliquen. Será necesario proporcionar una forma de realizar un seguimiento de qué SCR se incorporan, en qué versiones de software y líneas bases concretas. Como parte del cierre del proceso de cambios, los cambios realizados deben pasar por auditorías de configuración y verificación de la calidad del software. Esto incluye asegurar que sólo se han realizado los cambios aprobados.

La implementación del cambio será soportada por una herramienta que permita gestión de versiones y un repositorio de código.

Tras realizar el cambio se comunicará, si así está establecido, a todos aquellos que estén afectados por dicho cambio. De esta forma, se preservar la integridad de los productos haciendo que todo el mundo trabaje con las versiones correctas.

En el siguiente gráfico ilustra este proceso de control de cambios:

.. figure:: _static/controldecambios.png
    :scale: 80%
    :align: center

La autoridad para aceptar o rechazar los cambios propuestos reside en una entidad conocida como comité de control de configuración (CCB). Puede haber múltiples niveles de autorización de cambios dependiendo de varios criterios como la criticidad de los elementos implicados, la naturaleza del cambio (p.ej.: impacta en presupuesto o calendario), o el momento actual en el ciclo de vida. Las actividades del CCB están sujetas a revisión y auditoría de calidad de software.

Recuperación de los elementos de configuración
==============================================
	 	 	
En lo referido a la recuperación de los elementos de la configuración es preciso la definición de un repositorio general del proyecto que posea interfaz vía línea de comandos y/o gráfica y que en lo posible, también posea una interfaz web que facilite su uso. Además, la herramienta de repositorio deberá contar con una política de branching que no resulte dificultosa para el equipo.

La estructura del desarrollo se conformará por dos ramas principales:
	
    * master: esta 	rama contendrá todas las versiones estables del producto, con lo 	cual cualquier commit que se realice sobre ella, implica que el producto está listo para ser usado por los usuarios. Este paso 	implica que el producto haya pasado la correspondiente batería de pruebas y que esté debidamente documentado.
        
    * develop: en esta rama se aloja el código que conformará la siguiente la versión. Sobre esta rama se trabajará con versiones inestables, que buscan agregar los cambios necesarios para cumplir con los requerimientos.

Además de estas dos ramas principales se sugiere el uso de ramas de soporte. Dichas ramas son:

    * Feature: Nuevas características del producto.
    * Release: Últimos cambios antes de pasar a producción.
    * Hotfix: 	Cambios en “caliente”, corrección de bugs 	reportados mediante el uso de tickets en versiones del servicio que se encuentran en la rama master.	
    * Cleanup y Optimization: con estas ramas se busca fomentar las prácticas de limpieza y optimización de todos los productos.
		
Todas las ramas estarán sujetas a un esquema de nombrado, que permitan identificar cual ha sido la historia de la misma y cuál ha sido el motivo que ha dado origen a la rama. Se sugiere que las ramas adopten la siguiente forma: nombrerama/descripcion, en donde el nombrerama identifica alguna de las ramas antes presentadas y descripción es un texto breve que identifica al requerimiento.
	 	 	
Para las distintas ramas de soporte se definen un conjunto de reglas para su correcta utilización:
	 	 	
*Feature*

Se utilizan para desarrollar las nuevas características del servicio que, una vez terminadas, se incorporan a la rama develop.
Se dispara la creación de estas ramas a partir de nuevas funcionalidades que se espera del producto.
La utilización básica de estas ramas es la siguiente:

    * Se originan a partir de la rama develop, dado que se emplea el código que actualmente se está empleando.
    * Se incorporan siempre a la rama develop. Una vez hecho esto, se deberán eliminar las ramas ya no trabajaran sobre esa feature. De esta forma se busca un esquema de trabajo limpio en donde no se tenga constantemente múltiples ramas, sino que existan las ramas master y develop, y que el resto sean temporales.
    * El nombrado de esta rama puede ser cualquiera, pero no debe entrar en conflicto con el nombre de master, develop, relese o hotfix.  
	 	 	
*Release*

Estas ramas se utilizan para preparar el siguiente código en producción. Estas ramas son las que se vuelcan en los servidores de pre-producción para hacer el testing final: corrección de bugs, corrección de documentación, mejora de las GUI, etc. Se hace la puesta a punto final de la aplicación antes de liberar la versión definitiva, que irá a parar a la rama master y a la rama develop.
La utilización básica de esta rama es:

    * El nombrado de la rama deberá corresponder con un tag que se ajuste al esquema de identificación de versiones definido por el equipo.
    * Se originan a partir de la rama develop.
    * Se incorporan a master y develop. La rama dejará de existir una vez que se efectúe el merge sobre dichas ramas, con lo cual las versiones estables quedarán sobre la rama master y el trabajo en curso sobre la rama develop. En caso de existir bugs de último momento, se creará la rama de tipo Hotfix.
	 	 	
*Hotfix*

Estas ramas ayudan a hacer las modificaciones de forma más eficiente y a corregir el problema con el mínimo impacto sobre el resto del trabajo que se está haciendo. El uso de estas ramas permite:

    * Interrumpir el trabajo que se está haciendo en la rama develop para una versión nueva del servicio.	
    * Resolver el bug.	
    * Incorporar la 	 corrección del bug en la rama master para desplegarlo en producción lo más rápido posible. También permite identificar sobre la rama master que ha habido una corrección, modificando el número de patch en el identificador de la versión.	
    * Incorporar la 	corrección del bug en la rama develop, si es necesario.	
    * Retomar el trabajo en la rama develop. 	

	 	 	
*Cleanup*

Estas ramas son empleadas para la limpieza de todo lo producido, es decir, tanto a nivel de código como a nivel de documentación. En lo que respecta a la documentación, permite acomodar formato de la misma eliminación de errores de redacción, etc. A nivel de código permite eliminar piezas de código que no se ajusten a los estándares recomendados, que no cumplan con los requerimientos, etc.
	 	 	
*Optimization*

Estas ramas son empleadas para la optimización tanto a nivel de documentación como de código. En el caso de la documentación implica la reelaboración de aquella documentación que no se corresponda con la realidad. En el caso del código, implica la optimización de rutina de código sin impactar sobre la funcionalidad de la misma.

Informe del estado de los elementos de configuración
====================================================

El informe del estado de la configuración reporta la información necesaria para gestionar de forma efectiva la configuración de software. En esta actividad se deberá diseñar y operar un sistema para la captura y reporte de la información necesaria a medida que avanza el proceso de desarrollo.

Como en cualquier sistema de información, la información sobre el estado de la configuración que se quiere gestionar debe ser identificada, recogida y mantenida. Son necesarias diversas métricas e información para dar soporte al proceso de gestión de configuración. El tipo de información disponible incluye la identificación de configuración aprobada así como el estado actual de la implementación de los cambios. Por ejemplo, información del tipo:

    * Un registro de documentación de configuración aprobada.
    * La designación de un responsable de los elementos de configuración del proyecto.
    * El estado de cambios propuestos y desviaciones de la configuración.
    * La implementación del estado de los cambios aprobados.
    * La configuración de todas las unidades de los elementos de configuración en el inventario.
    * Resultados de las auditorías.

Para llevar a cabo estas actividades de obtención de datos y generación de informes se hace necesario el soporte de una herramienta automatizada.

Verificación y Auditoría
========================

Una auditoría de software es una actividad llevada a cabo para evaluar, de forma independiente y objetiva, la conformidad de los productos y procesos software con respecto a las regulaciones, estándares, guías, planes y procedimientos aplicables (IEEE1028-97). 

Las auditorías se llevarán a cabo de acuerdo a un proceso bien definido que detalla los roles y responsabilidades de los auditores. Cada auditoría debe ser cuidadosamente planificada, en función de la naturaleza del proyecto y de los requisitos. El uso de herramientas que ayuden en la planificación y realización de auditorías facilitan en gran medida el proceso.

Estas auditorías incluirán:

    * Objetivo: el objetivo de todas la auditorías es verificar que en un momento dada, la línea base se compone de una colección consistente y bien definida de productos.
    * Elementos de configuración bajo auditoría: se elegirán uno o más elementos de configuración de mayor prioridad en la línea base.
    * Agenda de auditorías: antes de la liberación o actualización.
    * Conducción: las auditorías serán dirigidas por el SCMR.
    * Participantes: SCMR y los autores de los elementos de configuración a auditar.
    * Documentos requeridos: documentos de SCR y reportes de estado de la configuración generados.
    * Reportes de deficiencias y acciones correctivas: determinadas por los participantes.
    * Criterio de aprobación: lo determina el SCMR.

La actividad de auditoría de configuración de software determinará en qué medida un elemento de configuración satisface sus características funcionales y físicas requeridas. Se pueden realizar auditorías de este tipo en puntos clave del proceso de desarrollo. El resultado satisfactorio de una auditoría se puede utilizar como prerrequisito para establecer una línea base del producto.

El objetivo de las auditorías de gestión de configuración es asegurarse de que:

    * Los elementos de configuración se encuentran en el directorio apropiado.
    * El estado actual de los elementos de configuración es consistente.
    * La información de línea base se mantiene de forma correcta.
    * Se verifica la conformidad con estándares y procedimientos aplicables a la gestión de configuración, por ejemplo, comprobando si se usa la versión correcta del documento de diseño para realizar la codificación.

Como resultado de la auditoría se deberá generar un informe donde se registren todas las no conformidades detectadas y así iniciar un plan de mejora para solucionarlas. Después de una auditoría de configuración exitosa se puede establecer una línea base del producto.

La verificación no se realiza sobre los propios productos sino que consiste en comprobar que los productos que conforman una línea base están gestionados correctamente bajo el control de configuración, que todos los cambios realizados sobre estos productos han sido registrados y, por tanto, se puede establecer una trazabilidad entre cambios y productos afectados.

Gestión de la liberación del Software
=====================================

El término liberación se utiliza en este contexto para referirse a la distribución del elemento de configuración de software fuera de la actividad de desarrollo. Esto incluye tanto liberaciones internas como distribuciones al cliente.

La gestión de la liberación del software implica la identificación, empaquetado y entrega de los elementos del producto, por ejemplo, programas ejecutables, documentación, notas de versión, y datos de configuración. Puesto que los cambios en el producto pueden producirse de forma continua, se deberá plantear cuándo lanzar una nueva versión. Esta decisión se tomará teniendo en cuenta la severidad de los problemas encontrados y la métrica de densidad de defectos registrada en la versión actual. En la tarea de empaquetado se deben identificar qué elementos del producto se van a entregar y las versiones correctas de esos elementos, según la aplicación deseada del producto. Las notas de versión describen las nuevas funcionalidades, problemas conocidos, y requisitos de la plataforma necesarios para la correcta operación del producto. El paquete que se va a liberar deberá contener también instrucciones para la instalación o actualización.

Identificación de Versiones
---------------------------

El esquema sugerido para la identificación de las distintas versiones del producto, es un esquema numérico conformado de la siguiente manera:

<major_version> . <minor_version> . <patch_number>

    * Major Version: indica un cambio de funcionalidad sustancial a otras versiones del sistema
    * Minor Version: indica que el sistema es funcionalmente idéntico, pero es distinto desde el punto de vista no-funcional a otras versiones
    * Patch Version: indica el número de un parche aplicado al sistema, que significa la corrección de un defecto encontrado

Herramientas
============

Se recomienda la utilización de las siguientes herramientas para llevar a cabo el plan de gestión de configuración del software:

    * Git: Sistema de control de versiones.
    * Github: Sistema web de control colaborativo de revisión y desarrollo de software utilizado para alojar proyectos que sean gestionados con Git.
    * Gitflow: Conjunto de extensiones de git que facilitan la gestión de ramas y flujos de trabajo. Provee una serie de hooks que automatizan la gestión de ramas en un repositorio git, permitiendo así trabajar con la estructura de ramas descrita en el plan.
