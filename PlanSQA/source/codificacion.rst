.. include:: global.rst

.. _codificacion:

**************************************
Codificación y Producción de Contenido
**************************************

Introducción
============

Esta sección se encargará de detallar los pasos, herramientas y buenas prácticas necesarias para la producción de código del sistema.

Alcance
=======

Esta sección comprende lo necesario para realizar buenas prácticas de codificación con HTML, CSS y JavaScript y programación en general.

Objetivos
=========

El objetivo principal de esta sección es promover el uso de estándares y buenas prácticas definidos y/o recomendados por la empresa, para el proceso de codificación y producción de contenido. Por contenido entiéndase: manual del sistema, manual del usuario, ayuda online, contenido web, entre otros. 

Aspectos de programación
========================

A continuación se definen los objetivos a alcanzar por aquellos programadores que participen del proyecto. Las producciones de código deberán aportar: 

* Facilidad para adicionar componentes y funcionalidades.
* Facilidad para hacer modificaciones al software. 
* Facilidad para corregir errores. 
* Facilitar seguimiento y ejecución de inspecciones de código. 
* Liberar la dependencia personal del código fuente. 
* Uso de un buen estándar de codificación que mejore la legibilidad del código y facilite la comunicación entre programadores. 
* Servir como punto de referencia para los programadores. 
* Unicidad con respecto al estilo de programación adoptado, siguiendo los estándares definidos más abajo en este documento. 
* Eficiencia al proceso de generación de código. 
* Un marco para implementar procedimientos de aseguramiento de la calidad. 
* Continuidad entre el trabajo de distintas personas. 

Como se mencionó previamente, en pos de mantener un estilo de programación homogéneo que favorezca la comprensión y mantenibilidad del código producido, se añade un compendio de estándares y/o buenas prácticas que los desarrolladores deberían tener en mente al momento de generar sus aportes.

Generación y/o limpieza de código
---------------------------------

* La codificación deberá respetar una misma convención idiomática. 
* Utilizar líneas en blanco en funciones para indicar secciones lógicas.
* El uso de líneas en blanco, para la separación de métodos,  debe ser utilizado con moderación.
* Utilizar un espacio de separación a cada lado entre los operadores binarios.
* Se deben usar dos líneas en blanco entre clases y definiciones de interfaz. 
* Se debe usar una línea en blanco entre métodos.
* Debe existir una sola instrucción por cada línea de código. 
* Se deberán seguir los estándares de codificación definidos para cada lenguaje o entorno de programación establecido por los desarrolladores.
* Los comentarios deberán respetar una misma convención idiomática.
* Los comentarios y la documentación del código deben mantener el mismo formato y criterio en todo el código. 
* Los comentarios deben ser oraciones completas. 
* Los comentarios en su primera palabra deben comenzar con mayúscula, a menos que sean identificadores que comienzan con una letra minúscula. 
* En los comentarios no se deben alterar los nombres de los identificadores.
* La estructura de la clase debe ser igual que la clase especificada en el diseño. 
* Todas las clases especificadas en el diseño deben estar presentes en el código. 
* La documentación del código se hará antes del inicio de cada método o inicio de cada clase. 
* La documentación del código debe añadir claridad al código. Debe contar el porqué o la finalidad y no el cómo. 
* Los comentarios se realizarán, solo en caso que sea necesario la comprensión del funcionamiento.
* Cuando una línea no quepa en una única línea se debe fraccionar atendiendo a estos principios generales: 
    
    Fraccionar después de una coma. 
    
    Fraccionar después de un operador. 

* Utilizar una misma indentación de caracteres para cada nueva línea generada. 
* Establecer un valor de longitud máxima para las líneas. 
* Mantener las importaciones en la parte superior del archivo, justo después de los comentarios del módulos y la documentación del código, y antes de la definición de las variables globales.
* Mantener una importación por línea.
* Para la asignación de nombres: 

    * Los desarrolladores van a convenir y dejar establecido la codificación de los nombres en algún lado del proyecto. 
    * Los desarrolladores deberán seguir los estándares universales de codificación de los lenguajes de programación utilizados y dejarlos establecidos en algún lugar del proyecto. 
    * Al definir una variable, debe ser completo y preciso para describir lo que representa. 
    * Evitar en lo posible los nombres demasiado largos (menos de 15 letras sería lo ideal) o demasiado cortos (más de 5 letras). 
    * Evitar nombres que difieren en una letra o en el uso de mayúsculas/minúsculas. 
    * Si el nombre consta de más de una palabra, la palabra siguiente deberá comenzar con mayúscula, o serán separadas por guión bajo. 

* Habrá un encargado de la investigación de nuevas tecnologías y herramientas para resolver problemas a lo largo de la codificación. 
* Realizar una correcta indentación de las estructuras de código, por medio de herramientas automatizadas. 

Refactoring y optimización 
--------------------------

* Métodos con nombres bien significativos (intention revealing, que revelen exactamente el propósito para el que fueron creados). 
* Métodos y clases con responsabilidades claras y bien definidas.
* Alta cohesión y bajo acoplamiento.
* Pocas variables de instancia: hay que evaluar el costo­-beneficio de tener en  variables valores que puedan calcularse, como el total de deuda de un cliente, o la  cantidad de hijos de un empleado.
* Hacer uso de patrones por ejemplo Singleton, MVC, etc. si se presenta un problema de estos tipos.
* Evitar tener objetos anémicos, con pocas responsabilidades que se parecen a  estructuras de datos. 
* Es preferible tener objetos simples antes que un objeto complejo con muchas  responsabilidades (sobre todo si los objetos simples pueden intercambiarse).
* Hacer uso de Herencia y Polimorfismo.
* Evitar ciclos de dependencia entre objetos si no son necesarios.
* Hacer uso de Excepciones para manejo de errores.
* Comentar el código extenso.
* Crear script (setup) para la instalación de todos los paquetes necesarios para poder usar la aplicación. Por ejemplo, en el caso de python se puede emplear la utilidad pip freeze sobre el directorio de trabajo para identificar todos los paquetes empleados por el software.
* Cuando el lenguaje empleado para realizar el desarrollo lo permita, emplear el/los estándar/es definidos actualmente. Por ejemplo, en el caso de Python se sugiere emplear el Estándar pep8 que define cuestiones como:
* Las líneas de continuación deben alinearse verticalmente con el carácter que se ha utilizado (paréntesis, llaves, corchetes) o haciendo uso de la “hanging indent” (aplicar tabulaciones en todas las líneas con excepción de la primera).
* Nunca mezcles tabulaciones y espacios.
* Las importaciones deben estar en líneas separadas.
* Las importaciones deben estar agrupadas en el siguiente orden:
			
    1. importaciones de la librería estándar

    2. importaciones terceras relacionadas

    3. importaciones locales de la aplicación / librería

* Evita usar espacios en blanco extraños.
* Siempre rodea estos operadores binarios con un espacio en cada lado: asignación (=), asignación de aumentación (+=, -=, etc.), comparaciones (==, <, >, !=, <>, <=, >=, in, not in, is, is not), “Booleans” (and, or, not).
* Si se utilizan operadores con prioridad diferente, considera agregar espacios alrededor del operador con la menor prioridad. Usa tu propio criterio, de todas maneras, nunca uses más de un espacio, y siempre mantén la misma cantidad en ambos lados.
* Las sentencias compuestas (múltiples sentencias en la misma línea) son generalmente desalentadas (poco recomendadas).
* Comentarios que contradigan el código es peor que no colocar comentarios. ¡Siempre realiza una prioridad de mantener los comentarios al día cuando el código cambie!
* Si un comentario es una frase u oración, su primera palabra debe comenzar con mayúscula, a menos que sea un identificador que comienza con minúscula. ¡Nunca cambies las mayúsculas/minúsculas de los identificadores! (Nombres de clases, objetos, funciones, etc.).
* Usa comentarios en línea (comentarios en la misma línea) escasamente. Los comentarios en línea son innecesarios y de hecho molestos si su acción es obvia.
* Los módulos deben tener un nombre corto y en minúscula. Guiones bajos pueden utilizarse si mejora la legibilidad. Los paquetes en Python también deberían tener un nombre corto y en minúscula, aunque el uso de guiones bajos es desalentado (poco recomendado).
* Las funciones deben ser en minúscula, con las palabras separadas por un guión bajo, aplicándose éstos tanto como sea necesario para mejorar la legibilidad.
* Las constantes son generalmente definidas a nivel módulo, escritas con todas las letras en mayúscula y con guiones bajos separando palabras.
* No compares valores del tipo boolean con True o False usando ==.
* Es recomendable limpiar el código, el código que ya no es útil debe eliminarse.
* En el caso de utilizar un framework como Django, la lógica de la aplicación debe estar contenida en el modelo (es la fuente única y definitiva de información de los datos. Contiene los campos y comportamiento esenciales de los datos que se están almacenando.) y no en las vistas (Cada vista es responsable de hacer una de dos cosas: Devolver un objeto HttpResponse con el contenido de la página solicitada o lanzar una excepción como Http404. Generalmente, una vista recupera datos de acuerdo a los parámetros que le hemos pasado, primero carga la plantilla y la rellena con los datos recuperados.).
* Es recomendable utilizar el archivo style.css para personalizar la apariencia de la aplicación.
* Es recomendable separar en Módulos, en lugar de tener un único archivo con todo el código.
* Es recomendable diseñar las interfaces de forma coherente:
* Evitar asignar nombres e iconos diferentes a botones con acciones similares.
* Evitar botones con fondo de color y botones sin fondo.
* Usar un solo idioma para el texto de los componentes de la interfaz.
* Es recomendable enmarcar los componentes pertenecientes a datos o acciones de un objeto determinado, para diferenciar de los de otro objeto que también está presente en la interfaz.
* Ubicar los componentes de la interfaz de forma que sea predecible la navegabilidad de la misma.
* Colocar los botones (cancelar o confirmar una operación) a la derecha de la interfaz o a la izquierda, no se pueden tener en una interfaz a la derecha y en otra a la izquierda, es molesto.

Codificación HTML, CSS y JavaScript
------------------------------------

En lo que refiere a la codificación en HTML, CSS y JavaScript se definen las siguientes recomendaciones:

* Declarar de forma correcta el DOCTYPE, para indicarle al navegador que versión se está empleando.
* Nombrar las etiquetas siempre en minúscula.
* Utilizar archivos externos para CSS y JavaScript, a fin de evitar modificaciones sobre el mismo archivo HTML.
* Se deberán cargar los CSS externos al principio.
* Se deberán cargar los JavaScript externos al final.

Así mismo, se deberá usar como referencia las recomendaciones establecidas por la W3C, para la correcta codificación de aplicaciones basadas en la web. Lo antes mencionado es un extracto de dichas prácticas, que fueron establecidas como prioritarias para este manual de calidad.

Aspectos de documentación
=========================

Todos los procesos del ciclo de vida del software en el desarrollo de cualquier producto se registran como documentación. La documentación sirve como información escrita sobre definición de requerimientos, especificaciones generales del sistema, especificación de cada componente y los planes integrales de prueba y mantenimiento. Las herramientas de gestión de configuración también son de gran utilidad en la documentación del software.

Recomendaciones:

* Se recomienda seguir algún estándar de documentación existente (por ejemplo, ISO/IEC , 26514:2008, IEEE 1063-2001, etc).
* Debe emplear un lenguaje que sea entendido por todos los usuarios finales, sin dar lugar a segundas interpretaciones.
* El lenguaje debe ser adecuado al dominio de la aplicación.
* Cada párrafo debe expresar claramente una idea.
* La información presentada debe ser exacta y precisa.
* En caso de manual de usos, debe poseer una organización de contenidos ordenada y un índice detallado.
* Debe documentar conceptos puntuales y estables, no ideas especulativas.
* Debe escribir los documentos con mìnimo solapamiento.
* Si se utiliza una tecnología específica para desarrollar el código del producto, se deben seguir los estándares de esa tecnología.
* El documento debe poseer un propósito.
* Debe centrarse en las necesidades de los clientes finales actuales.
* Se debe actualizar sólo cuando sea necesario.
* La documentación debe ser tratada como un requisito.	 	 	
* En caso de utilizar un manual de usuario, para confeccionarlo se debe recurrir a una persona con experiencia en la redacción de los mismos.	 	 	
* Se debe documentar de manera completa y detallada los requisitos mínimos para poder utilizar el producto final.

Aspectos Estéticos
==================

Las recomendaciones tratan de cumplir con los siguientes objetivos:

* Que las distintas páginas que componen a la aplicación se visualicen de forma rápida y sin dificultades técnicas en los equipos de los usuarios.
* Que las páginas se puedan visualizar de forma correcta en cualquier dispositivo, respetando la coherencia con que fueron creadas.

Los criterios estéticos a emplear para la elaboración de la aplicación:

* Los distintos componentes de la página deben estar agrupados, de manera tal que los mismos correspondan a una única funcionalidad.
* Se deberá destacar aquellas operaciones que sean trascendentales, mediante el uso de colores e/o iconos representativos. Por ejemplo, la operación de Añadir deberá sobresalir por sobre otras.
* Se deberá hacer un buen uso del espacio visual de la página.
* La fuente empleada para expresar el texto debe permitir la legibilidad de la página.
* Deberán existir zonas en blancos que posibiliten descansar.
* Se deberá destacar los mensajes de advertencia  y error generados por la aplicación, por sobre otros mensajes.

Métricas Sugeridas
==================

A fin de evaluar el trabajo del equipo durante el proceso de desarrollo, se sugiere emplear el enfoque de Halstead para obtener métricas sobre la longitud y volumen de los diferentes módulos que se generen  (entre otras). Las métricas que se sugieren emplear son:

* Para la longitud del programa:
    
    N = N1 + N2

* Para el vocabulario del programa:

    nt = n1 + n2

* Para el volumen del programa:

    V = N log2 (n1 + n2)
 
* Para la dificultad del programa:
    
    D = (n1 * N2 ) / (2 * n2 )	

* Para el esfuerzo:

        E = V * D

    n1: el número de operadores diferentes que aparecen en el programa
    n2: el número de operandos diferentes que aparecen en el programa
    N1: el número total de veces que aparece el operador
    N2: el número total de veces que aparece el operando

**Complejidad Ciclomática**: Es una métrica del software que proporciona una medición cuantitativa de la complejidad lógica de un programa. Es una de las métricas de software de mayor aceptación, ya que ha sido concebida para ser independiente del lenguaje.

Una vez calculada la complejidad ciclomática de un fragmento de código, se puede determinar el riesgo que supone utilizando los rangos definidos en la siguiente tabla:

+-------------------------------+----------------------------------------+
| **Complejidad Ciclomática**   | **Evaluación del Riesgo**              | 
+===============================+========================================+
| 1-5                           | Programa Simple, sin mucho riesgo      |
+-------------------------------+----------------------------------------+
| 11-20                         | Más complejo, riesgo moderado          |
+-------------------------------+----------------------------------------+
| 21-50                         | Complejo, Programa de alto riesgo      |
+-------------------------------+----------------------------------------+
| > 50                          | Programa no testeable, Muy alto riesgo |
+-------------------------------+----------------------------------------+

A partir del análisis de muchos proyectos se encontró que un valor 10 es un límite superior práctico para el tamaño de un módulo. Cuando la complejidad supera dicho valor se hace muy difícil probarlo, entenderlo y modificarlo.

La complejidad ciclomática tiene fundamentos en la teoría de gráficos y proporciona una medición de software extremadamente útil. 

La complejidad se calcula en una de tres formas:

1. El número de regiones del gráfico de flujo corresponde a la complejidad ciclomática.

2. La complejidad ciclomática V(G) para un gráfico de flujo G se define como V(G) = E - N + 2 donde E es el número de aristas del gráfico de flujo y N el número de nodos del gráfico de flujo.

3. La complejidad ciclomática V(G) para un gráfico de flujo G también se define como V(G) = P + 1 donde P es el número de nodos predicado contenidos en el gráfico de flujo G. 

En definitiva, la complejidad ciclomática (V(G)) por método o función representa el grado de facilidad o dificultad para entender modificar o corregir un método o función dentro de un programa. Esta complejidad aumenta con el número de caminos que el programa pueda seguir. Se recomienda mantener éste valor menor a 6

Herramientas
============

Las herramientas que se sugieren para la producción de código son:

* Pycharm: entorno de desarrollo para Python que permite gestionar fácilmente la estructura del proyecto, la escritura de código (provee autocompletado) y cuestiones adicionales como manejo de Git integrado.

* Sublime + plugins Anaconda for Python: editor de texto base que permite escribir código Python haciendo uso de los bondades que ofrece una serie de plugins adicionales, como Anaconda, que permiten el autocompletado, la detección de errores y otras características.

* Flake: herramienta para Python que permite determinar si un fuente cumple con la especificación PEP8 recomendada anteriormente. Aquellos aspectos que no cumplen, son marcados para su corrección.

* Sphinx: herramienta que permite la construcción de la documentación de manera inteligente y agradable tanto para los usuarios como los programadores. Provee una serie de extensiones para la inclusión de los docstrings de Python, estructuración jerárquica de contenido con posibilidad de links y otras características.

* Sass o Less: cuando el CSS empleado a lo largo del proyecto sea demasiado y muchas veces repetitivo, se sugiere el empleo de un lenguaje dinámico de CSS que permite la escalabilidad del mismo.

* Radon: Herramienta de python que calcula varias métricas del código. Puede utilizarse desde la línea de comandos o mediante programación a través de su API