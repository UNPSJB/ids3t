.. include:: global.rst

.. _pruebas:

*******
Pruebas
*******

Introducción
============

En esta sección se detalla el plan de pruebas que se utilizará para planear y controlar los esfuerzos de pruebas del proyecto.   

Alcazce
=======

Esta sección cubre la confección del plan de pruebas, detalles de cada prueba y resultados que debería proveer.

Objetivo
========

Esta sección estructura y documenta la planificación de las pruebas del sistema a realizar, así como la estrategia a utilizar para su ejecución.

Plan de prueba
==============

El propósito del plan de pruebas es proveer la información necesaria para planear y controlar los esfuerzos de pruebas de un proyecto o iteración específicas. Describe el enfoque para probar el software  y es el plan general generado y utilizado por administradores para dirigir el esfuerzo de pruebas.

Se debe tener en cuenta, a la hora de definir un plan de prueba, que es lo que se va a probar, es decir describir el objeto de prueba y que es lo que se va a probar del mismo (una lista de las características y descripción del sistema, sus componentes tomados por separado, etc).

Se debe establecer qué estrategias se van a utilizar para las mismas (técnica, patrones y/o herramientas a utilizar). Por ejemplo, en el caso de pruebas unitarias de un procedimiento, esta sección podría indicar: "Se aplicará la estrategia caja-negra de fronteras de la precondición" o "Ejercicio de los caminos ciclomaticos válidos". En lo posible, la estrategia debe precisar el número mínimo de casos de prueba a diseñar; por ej. 100% de las fronteras, 60% de los caminos ciclomaticos, etc. La estrategia también explicita el grado de automatización que se exigirá, tanto para la generación de casos de prueba como para su ejecución. 

Se deberán establecer las secuencias de actividades, como la definición de los tiempos para la preparación de las pruebas, la ejecución de las pruebas hasta el análisis de resultados de la pruebas en el contexto de las fases previstas del desarrollo. Además se deberá disponer de toda la documentación necesaria, la plataforma de pruebas preparada (banco de pruebas) y la integridad del desarrollo de la funcionalidad requerida.

Se deberá categorizar la configuración, es decir explicitar las condiciones bajo las cuales, el plan debe ser: 

Suspendido.
Repetido.
Culminado.

En algunas circunstancias (las cuales deben ser explicitadas) el proceso de prueba debe suspenderse en vista de los defectos o fallas que se han detectado. Al corregirse los defectos, el proceso de prueba previsto por el plan puede continuar, pero debe explicitarse a partir de qué punto, ya que puede ser necesario repetir algunas pruebas. Los criterios de culminación pueden ser tan simples como aprobar el número mínimo de casos de prueba diseñados o tan complejos como tomar en cuenta no sólo el número mínimo, sino también el tiempo previsto para las pruebas y la tasa de detección de fallas. 

Se tendrán que explicitar los documentos a entregarse al culminar el proceso previsto por el plan de prueba por ejemplo: subplanes, especificación de pruebas, casos de prueba, resumen gerencial del proceso y bitácora de pruebas. 

Este plan de pruebas soporta los siguientes objetivos:

Identificar los ítems a probar
Describe, en términos generales, el enfoque de pruebas a ser usado
Identifica los recursos requeridos y provee un estimado de sus esfuerzos
Lista los entregables de las pruebas del proyecto
Identificar los tipos de pruebas a utilizar en la ejecución de las mismas.
Diseñar cada una de las pruebas de cada una de las iteraciones a probar.

Tipos de prueba
---------------

Pruebas de la implementación y de unidad
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Será objeto de estas pruebas verificar la funcionalidad y estructura de cada componente individualmente, una vez que estos han sido codificados.
Para poder llevar a cabo estas pruebas es preciso:

Garantizar que el proceso de codificación, las revisiones asociadas y la prueba de unidad sean conducidos de acuerdo a los estándares y procedimientos  establecidos en el plan de proyecto.
Asegurar la incorporación de los resultados de las revisiones en los entregables de esta fase.
Verificar la implementación de las acciones correctivas derivadas de la prueba de unidad.
Comprobar la utilización de la especificación de procedimientos y casos de prueba durante la prueba de unidad. 	
Corroborar la documentación del código y de los resultados de la prueba de unidad.


Objetivo de la Prueba:
Se focaliza en ejecutar cada módulo (o unidad mínima a ser probada, ej = una clase) lo que provee un mejor modo de manejar la integración de las unidades en componentes mayores.
Busca asegurar que el código funciona de acuerdo con las especificaciones y que el módulo lógico es válido.

Responsable:



Pasos:
El encargado de diseñar y realizar esta prueba puede ser uno de los desarrolladores del sistema.  

1. Determinar el ambiente de prueba.
2. Particionar el sistema en módulos de unidades lógicas fáciles de probar.
3. Por cada unidad hay que definir los casos de prueba (pruebas de caja blanca).
4. Para esto los casos de prueba deben diseñarse de forma tal que se recorran todos los caminos de ejecución posibles dentro del código bajo prueba; por lo tanto el diseñador debe construirlos con acceso al código fuente de la unidad a probar.
5. Los aspectos a considerar son los siguientes: Rutinas de excepción, Rutinas de error, Manejo de parámetros, Validaciones, Valores válidos, Valores límites, Rangos, Mensajes posibles.

Técnica:
Comparar el resultado esperado con el resultado obtenido.
Si existen errores, reportarlos.
Criterio de Completitud:
Todas las pruebas planeadas han sido ejecutadas.
Todos los defectos que se identificaron han sido tenidos en cuenta.

Pruebas de Integración
^^^^^^^^^^^^^^^^^^^^^^

Será objeto de estas pruebas verificar el correcto ensamblaje de los distintos módulos que componen la aplicación, una vez que han sido probados unitariamente, con el fin de comprobar que interactúan correctamente a través de sus interfaces internas y externas, que cubren la funcionalidad establecida y se ajustan a los requisitos no funcionales.

Las pruebas deberán asegurar que:

El funcionamiento integrado de módulos interdependientes esté libre de errores.
Probar todas las dependencias de los módulos.
Probar el flujo de control y el flujo de datos a través de todas las capas


Para llevar a cabo dichas pruebas, se empleará un enfoque de Pruebas de Integración Incremental Ascendente, en donde se ejecutarán las siguientes actividades:

La combinación de módulos de bajo nivel en grupos que lleven a cabo una misma función o subfunción específica, con el fin de reducir el número de pasos de integración.
La escritura de módulos impulsores para cada módulo, con el fin de simular la llamada a los módulos, introducir los datos de pruebas y recoger los resultados.
La prueba de cada módulo con su correspondiente módulo impulsor.
La eliminación de los módulos impulsores y su correspondiente sustitución por los módulos de nivel superior en la jerarquía.

Integración Descendente: Se integran los módulos moviéndose hacia abajo por la jerarquía de control, comenzando por el módulo de control principal (programa principal). Los módulos subordinados al módulo de control principal se van incorporando en la estructura, bien de forma primero en profundidad, o bien de forma primero en anchura.

 
Integración primero en profundidad: integra todos los módulos de un camino de control principal de la estructura. Por ejemplo, si se elige el camino de la izquierda se integrarán primero los módulos M1, M2 y M5. A continuación, se integrará M8 o M6. A continuación se construyen los caminos de control central y derecho.

Integración primero en anchura: incorpora todos los módulos directamente subordinados a cada nivel, moviéndose por la estructura de forma horizontal.
Por ejemplo: Los primeros módulos que se integran son M2, M3 y M4. A continuación, sigue el siguiente nivel de control, M5, M6, M7 y por último M8.

El proceso de integración se realiza en cinco pasos:

1. Se usa el módulo de control principal como controlador de la prueba, disponiendo de resguardos para todos los módulos directamente subordinados al módulo de control principal.
2. Dependiendo del enfoque de integración elegido se van sustituyendo uno a uno los resguardos subordinados por los módulos reales.
3.  Se llevan a cabo pruebas cada vez que se integra un nuevo módulo.
4. Tras terminar cada conjunto de prueba, se reemplaza otro resguardo con el módulo real.
5. Se hace la prueba de regresión para asegurarse de que no se han introducido errores nuevos.

El proceso continúa desde el paso dos hasta que se haya construido la estructura del programa entero.

Integración Ascendente: Empieza la construcción y la prueba con los niveles más bajos de la estructura del programa. Dado que los módulos se integran de abajo hacia arriba, el proceso requerido de los módulos subordinados siempre está disponible y se elimina la necesidad de resguardos.

La integración sigue el esquema de la siguiente figura:



El proceso de integración se realiza mediante los siguientes pasos:

1. Se combinan los módulos de bajo nivel en grupos que realicen una subfunción específica del software.
2. Se describe un controlador (un programa de control de la prueba) para coordinar la entrada y la salida de los casos de prueba.
3. Se prueba el grupo.
4.  Se eliminan los controladores y se combinan los grupos moviéndose hacia arriba por la estructura del programa.

Se combinan los módulos para formar los grupos 1,2 y 3. Cada uno de los grupos se somete a prueba mediante un controlador (mostrado como un bloque punteado). Los módulos de los grupos 1 y 2 son subordinados Ma. Los controladores D1 y D2 se eliminan y los grupos interaccionan directamente con Ma. De forma similar, se elimina el controlador D3 del grupo 3 antes de la integración con el módulo Mb. Tanto Ma como Mb se integrarán finalmente con el módulo Mc y así sucesivamente

Pruebas de Regresión
^^^^^^^^^^^^^^^^^^^^

Será objeto de estas pruebas validar que el sistema mantenga su correcta funcionalidad después de que se efectúe un cambio, corrección o nuevo requerimiento.

Para poder llevar a cabo dicha prueba es preciso:

Repetir la batería de pruebas (las pruebas unitarias, de integración, funcionales y de carga) definidas con anterioridad al cambio efectuado, para comprobar que la incorporación de los ajustes no crearon errores en el sistema. 

Pruebas de Stress
^^^^^^^^^^^^^^^^^

Será objeto de estas pruebas conocer y mitigar los riesgos relacionados con el mal desempeño de las aplicaciones en el entorno, y efectuar las correcciones necesarias.

Para poder llevar a cabo estas pruebas es preciso:

Cuantificar la capacidad de la infraestructura.
Validar los requerimientos de performance.
Validar la escalabilidad de la plataforma.

Con la definición de estos criterios, se podrá conocer qué cantidad de clientes simultáneos soporta el producto desarrollado y si el hardware empleado es suficiente para soportar el nivel de transacciones propuesto. Además, se podrá evaluar què expectativa de crecimiento soporta el producto.

Pruebas de Aceptación
^^^^^^^^^^^^^^^^^^^^^

Será objeto de estas pruebas validar que la solución desarrollada cumpla con el funcionamiento esperado y permitirle al usuario del sistema que verifique su aceptación, desde el punto de vista de la funcionalidad y el rendimiento.

Para llevar a cabo esta prueba será preciso reunirse con el usuario y probar el software de manera conjunta, registrando aquellos aspectos negativos que indique el usuario y posibles sugerencias.





Pruebas del proceso de SCM (Gestión de Configuración)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Será objeto de estas pruebas asegurar y garantizar un adecuado control del proceso de los cambios realizados sobre el producto y la disponibilidad constante de una versión estable de cada elemento para toda persona involucrada en el desarrollo 

En este tipo de pruebas el SQA debe:

Revisar el plan de SCM.
Asegurar la correcta identificación de los ítems de configuración.
Garantizar un adecuado control de cambios.
Corroborar que la contabilidad del estado de la configuración sea preparada oportunamente y que refleje la situación real de los ítems de configuración en relación con el proyecto.
Comprobar la adherencia de las actividades de SCM al plan de SCM.
Verificar el correcto funcionamiento de la librería del software.

Criterios de aceptación
-----------------------

No se acepta documentación con errores ortográficos.
No se acepta documentación con un grado de completitud menor al 70% con respecto a los issues del producto.
No se aceptan las pruebas unitarias que no cumplan los objetivos esperados.
No se aceptan las pruebas de integración en las que alguna de las pruebas unitarias falle o como resultado final, no se cumpla la funcionalidad establecida en el requerimiento.
No se aceptan las pruebas de regresión las cuales luego de corregir/agregar una funcionalidad arrojen un resultado distinto.
 
Para cada uno de estos ítems, cabe destacar que se acepta el caso contrario al mismo, por ejemplo “Se acepta documentación sin errores ortográficos”.

Equipo de Pruebas
-----------------

La asignación de los roles para los integrantes del equipo de pruebas será:

Test Lead 
Esta   es   la   persona   responsable   de   la   supervisión   de   las   pruebas   en   el   proyecto.   También   es  
responsable de los procesos utilizados para garantizar la calidad de la entrega. 
 
● Coordinación del equipo de pruebas. 
● Representación del equipo de pruebas en varias reuniones. 
● La generación de diversos informes. 
● La identificación de riesgos, análisis y mitigación. 
● Presentar Informes sobre cambios al Test Manager sobre el progreso de la prueba. 
● Gestión del repositorio. 
 
Test Manager 
● Escribe el plan de pruebas. 
● Realiza el mantenimiento del plan de prueba. 
● Monitorea el progreso de las prueba. 
● Toma decisiones sobre la entrada y salida de una prueba. 
● Toma decisiones sobre la suspensión / reanudación de las pruebas. 
● Toma decisiones sobre cambios en la estrategia de prueba / plan de pruebas. 
 
Business Analyst 
● Identificar escenarios adecuados para el test de aceptación de usuario. 
● Crear casos de pruebas para los test de aceptación de usuario. 
● Realizar pruebas funcionales. 
● Trabajar con el cliente para definir los requerimientos del negocio. 
 
Developers 
● Realizar pruebas unitarias. 
● Ejecutar las pruebas unitarias. 
● Revisiones de código 
● Crea los casos y los datos de prueba del sistema. 
● Administrar   el   tiempo   a   la   programación   del   proyecto   para   que   todas   las   tareas asignadas se completen a tiempo. 
 
Tester 
● Ejecutar el plan de pruebas. 
● Buscar, informar y seguir errores descubiertos durante las pruebas del sistema. 
● Analizar los resultados. 
Realizar Control de la conformidad con:los estándares de codificación, Ayuda  (online, manuales),Pruebas de Navegación, la experiencia del usuario y   pruebas de usabilidad, pruebas de rendimiento, las pruebas de compatibilidad   de plataforma, la prueba de escalabilidad, copia de seguridad   y   restauración,   las pruebas de instalación. 

Suspensión y reanudación
------------------------ 

Cuando se lleve a cabo la ejecución de un set de pruebas y alguno de los elementos de prueba falle (no pase la prueba), se notificará a los responsables del desarrollo de dicho elemento y se suspenderá la prueba hasta tanto se solucionen los inconvenientes.
Al momento de reanudar las pruebas suspendidas se deberá evaluar, según la complejidad del caso, la necesidad de ejecutar el set de pruebas nuevamente o reanudar desde el punto en el cual se había suspendido.
 
Entregables de prueba
---------------------

Los distintos entregables de las pruebas son:
● Especificación del diseño de pruebas.
● Especificación de casos de prueba.
● Especificación del procedimiento de prueba.
● Resumen del informe de prueba.
● Los datos de entrada y salida de las distintas pruebas.
● Logs de errores.
 
Necesidades ambientales
-----------------------

Serán necesarios para un correcto aislamiento de todas las fases en las que puede encontrarse cada versión del sistema, contar con distintos entornos para la ejecución y pruebas del sistema

Desarrollo
^^^^^^^^^^

Entorno altamente volátil. Los datos serán ingresados por los mismos desarrolladores de acuerdo a las funcionalidades que vayan desarrollando. Es el ambiente de pruebas que utilizarán los desarrolladores
 
Pruebas
^^^^^^^

Ambiente de Prueba:
Un BackUp completo antes de la ejecución de cualquier caso de prueba.
Al finalizar una jornada de pruebas se realiza un backup incremental.
Al detectar errores de impacto “Crítico” en la aplicación, se realizará backup completo e inmediato de la base de datos  y del sitio de la aplicación, asociándolo a un documento descriptivo del escenario y del caso de prueba que se estaba llevando a cabo. Esto con el fin de poder reproducir estos errores posteriormente sobre un ambiente controlado y facilite la detección de la causa y la corrección del mismo.
 
Producción
^^^^^^^^^^

Entorno de producción en el que se encontrarán los datos reales y ejecutables estables.
Excede el entorno de pruebas.


Aspectos de ejecución de las pruebas
------------------------------------

Aspectos de entrada y salida
^^^^^^^^^^^^^^^^^^^^^^^^^^^^ 

Plan de Prueba, Aspectos de Entrada
 
Una vez desarrollado cada uno de los módulos del aplicativo se comenzará a realizar el set de pruebas.
Set de pruebas completo y claro.
Claridad en el procedimiento para el desarrollo de las pruebas.
Tener un entorno de pruebas adecuado.
Toda la documentación requerida para la realización de las pruebas debe estar disponible.

Plan de  Prueba, Aspectos de Salida

El sistemas será sometido a 3 ciclos de pruebas: 1)Pruebas a cada módulo, 2) Pruebas luego de la integración entre módulos, y 3) Pruebas después de corregir  las fallas del segundo ciclo, este último con el fin de asegurar que la corrección  de errores no haya generados unos nuevos.

Definición del Entorno de Pruebas
---------------------------------

El plan de pruebas recogerá las características que debe tener el entorno para la ejecución de pruebas según la información existente del proyecto en el momento de la elaboración del plan. 

Se debe describir el entorno general de las pruebas y en concreto las posibles configuraciones de hardware a utilizar en las pruebas, así como las configuraciones de software y/o combinaciones de ambos.

Se debe describir la infraestructura que se utilizará para realizar las pruebas, indicando todos los sistemas/subsistemas que se utilicen.

Los elementos bases siguientes del software se requieren en el ambiente de la prueba para  este plan de prueba.

Nombre del elemento software
Versión
Tipo y otras notas
Sistema operativo Windows o distribución Linux.
Windows 7 o superiores.
Distros Linux:  -Debian/Ubuntu/Kubuntu
-------------------------------------
Navegador web
Chrome/Firefox/Opera
-------------------------------------
Gestor de Base de Datos
PostgreSql, MySql, SQLlite3
-------------------------------------
Herramienta para el seguimiento de errores
Bugzilla

Conjunto de datos
-------------------------------------
Mínimamente se definirán un conjunto de datos que pongan a prueba los casos bordes. 

Definir el Alcance y la Estrategia de Pruebas
---------------------------------------------

En esta tarea se especifican y justifican de los niveles de pruebas a realizar, así como el marco general de planificación de cada nivel de prueba, según el siguiente esquema:
Definición de los perfiles implicados en los distintos niveles de prueba.
Planificación temporal.
Criterios de verificación y aceptación de cada nivel de prueba.
Definición, generación y mantenimiento de verificaciones y casos de prueba.
Análisis y evaluación de los resultados de cada nivel de prueba.
Productos a entregar como resultado de la ejecución de las pruebas.

Registro de pruebas
===================

Descripción
-----------

El registro de pruebas es un mecanismo empleado para tener un control detallado sobre las pruebas realizadas en el sistema almacenando datos importantes para: resolución de problemas, análisis de los procedimientos de desarrollo y mejoramiento de la calidad del software a nivel general. Es necesario evaluar el proyecto a medida que se va construyendo, por lo tanto se hace necesario llevar a cabo, en paralelo al proceso de desarrollo, un proceso de evaluación o comprobación de los distintos productos o modelos que se van generando.

Entradas del registro
---------------------

Ejecuciones: Se identificarán las ejecuciones realizadas sobre el sistema. Se deberá indicar el número de ejecución de la prueba, la fecha de la ejecución de la misma y algún identificador que identifique unívocamente la prueba.

Resultados del procedimiento: Al final de cada prueba se indicarán los resultados obtenidos, destacando número de pruebas pasadas con éxito, número de pruebas con resultados fallidos y número de pruebas totales. A modo de complemento, debería adjuntarse, si es necesario, un listado con las pruebas ejecutadas seguido de su resultado. 
Por ejemplo: 
Alta cliente Ok
Alta Servicio Fail

Información sobre el ambiente de prueba:  Se detallará el ambiente utilizado para realizar las pruebas. Se describirá el entorno general de pruebas y en concreto las posibles configuraciones de hardware a utilizar en las pruebas, así como las necesidades software y/o combinaciones de ambos.

Eventos anómalos
Se adjuntará además lo producido por lo detallado en la siguiente sección.
5.6 Informe de pruebas: Incidencias
Todas las pruebas realizadas debieran tener una referencia al identificador de un caso de prueba, de modo tal, que sea posible establecer una relación entre ambos y además,  favorece a la trazabilidad del requerimiento ya que el propio caso de prueba tendrá un claro punto de orígen/creación, con lo cual será posible saber en todo momento el estado en el que se encuentra una prueba y/o un caso de prueba.

5.7 Herramientas
Las herramientas que se sugieren para la realización del proceso de prueba son:

PyUnit
Splinter
Unittest.mock
Doctest
Selenium

Breve descripción de las herramientas:


PyUnit

Este marco de pruebas unitarias, apodado “PyUnit” por convención, es una versión en Python de JUnit.JUnit fue escrito por Kent Bleck y Erich Gamma, y es a su vez, una versión Java del marco de pruebas de Smalltalk de Kent. Cada uno es el el framework de pruebas estándar de facto para su respectivo lenguaje y por lo tanto ambos son una base para un marco Python eficaz y elegante.

Splinter

Splinter, es una herramienta open source para hacer testing de aplicaciones web usando Python. Este framework te permite automatizar acciones del navegador, como visitar páginas web e interactuar con sus elementos. Dado que Splinter nos permite automatizar acciones en el navegador, puede emplearse para realizar pruebas en aplicaciones escritas no solo en Python. Splinter no está integrado a ningún framework de pruebas de aceptación pero posee una capa de abstracción para escribir su propia implementación.

Unittest.mock

Unittest.mock es una biblioteca para realizar pruebas en Python. Esta le permite reemplazar partes de su sistema bajo prueba con objetos simulados y hacer afirmaciones sobre la forma en que se han utilizado. Después de realizar una acción, puede hacer afirmaciones sobre los que utilizaron métodos/atributos y argumentos con los que se les llama. Mock es muy fácil de usar y está diseñado para su uso con unittest. Mock se basa en el patrón “acción -> afirmación” en vez de “record -> replay” utilizado por muchos mocking frameworks.

Doctest 

Python tiene un soporte considerable para pruebas, con los módulos doctest y unittest para pruebas de unidad y el módulo de pruebas para pruebas de regresión.
Cuando creamos un módulo, estos están diseñados para ser importados y los objetos ser proveídos. Cuando el módulo es importado las pruebas de unidad simplemente son ignorados; pero cuando el módulo está siendo ejecutado las pruebas de unidad son ejecutados. Estas acciones son llevadas a cabo gracias al módulo doctest.
El módulo doctest nos permite realizar pruebas unidad de la manera más simple y fácil como sea posible.
Para realizar las pruebas todo lo que necesitamos es adicionar ejemplos a nuestro docstring, escribiendo lo mismo que en el intérprete de Python y el resultado que quisiéramos obtener de retorno. 
El docstring contiene una pequeña descripción de lo que se intenta probar, seguido del código que hubiéramos tipeado para realizar la prueba en el intérprete de Python.
El módulo doctest usa esta sintaxis ya que nos es más familiar.




Ejemplo de uso:
python NombreDelPrograma.py -v

Selenium

Selenium es un conjunto de utilidades que facilita la labor de obtener juegos de pruebas para aplicaciones web. Para ello nos permite grabar, editar y depurar casos de prueba, que podrán ser ejecutados de forma automática e iterativa posteriormente.
Además de ser una herramienta para registrar acciones, permite editarlas manualmente o crearlas desde cero. Las acciones se basan en el uso de diferentes API's en diferentes lenguajes (PHP, Ruby, JAVA, Javascript, etc). Entre su principales características podemos nombrar:
Facilidad de registro y ejecución de los test.
Referencia a objetos DOM en base al ID, nombre o a través de XPath.
Auto-completado para todos los comandos.
Las acciones pueden ser ejecutadas paso a paso.
Herramientas de depuración y puntos de ruptura (breakpoints).
Los test pueden ser almacenados en diferentes formatos.

El potencial de esta herramienta puede ser utilizado para la grabación de las pruebas funcionales durante la Generación de pruebas de regresión. Con este servicio se consigue obtener una batería de pruebas automatizadas que podrán ser utilizadas cuando sea necesario repetir las pruebas.
