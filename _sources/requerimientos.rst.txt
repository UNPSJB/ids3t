.. include:: global.rst

.. _requerimientos:

****************************
Ingeniería de Requerimientos
****************************

Introducción
============

Esta sección es una guía de gestión de requerimientos para el sistema. Contiene todo requerimiento que altere el proyecto o el producto.

Alcance
=======

La gestión de requerimientos comprenderá requisitos relacionados con el producto de software y con el proyecto en general.

Objetivos
=========

* Minimizar los riesgos del proyecto, producto o proceso.
* Mejorar y garantizar la calidad de los mismos.
* Reducir los costes totales.
* Mejorar la comunicación entre las partes interesadas

Atributos generales de los requisitos
=====================================

*Identificador único*: Para permitir la trazabilidad, todo requisito debe tener un identificador que no debe cambiar a lo largo de su ciclo de vida, o al menos no debe cambiar una vez que el requisito se incluya en una línea base. Aunque un requisito se elimine, su identificador no debe reutilizarse, sobre todo si el requisito ha formado parte de alguna línea base.

Existen múltiples alternativas para la construcción de identificadores únicos de requisitos. La mayoría suelen estar formadas por una etiqueta (denominada en algunas herramientas de gestión de requisitos como contador) y un número secuencial, por ejemplo: IRQ-0001, MAD-CU-0062, ACZ-GO-FRQ-0039, etc.

En caso de que exista una descomposición jerárquica de requisitos, si el padre tiene el identificador ID-XXX, sus requisitos hijos pueden utilizar ese mismo identificador seguido de un punto y un número secuencial.

*Descripción*: Describir brevemente el motivo del requerimiento.

*Nombre descriptivo*: Normalmente, aparte de un identificador único, los requisitos suelen atribuirse con un nombre corto para hacer referencia a ellos de forma algo más humana que si sólo se usará el identificador. Es precisamente la dificultad de generar nombres únicos lo que hace imprescindible a los identificadores únicos.

*Información de versión*: Los requisitos deben estar bajo control de configuración, por lo que se van generando diferentes versiones a lo largo de un proyecto. Para evitar confusiones entre distintas versiones de un mismo requisito, es importante conocer el número o etiqueta de la versión de un requisito (por ejemplo 1.0, 2.3, etc.) y la fecha en que se creó dicha versión.

En el caso de que no se dispongan de herramientas de gestión de requisitos que permitan un control de configuración a nivel de requisitos individuales, la versión de los requisitos puede hacerse coincidir con la versión del documento en el que se describen.

*Trazabilidad*: Para mantener la trazabilidad, los requisitos deben estar convenientemente trazados hacia adelante y hacia atrás en el proceso de desarrollo. Así, se suelen mantener las trazas hacia:

    
    * Autores: son los autores del requisito. Lo habitual es atribuir los requisitos con el nombre y organización a la que pertenecen las personas que lo han redactado. Esta información es importante para poder gestionar posibles disconformidades de calidad de los requisitos y para solventar dudas o conflictos que puedan surgir.  
    * Fuentes: son las personas (casi siempre clientes y/o usuarios) o documentos que han proporcionado información sobre el requisito. Esta información es importante para poder solventar posibles dudas o conflictos que puedan surgir.
    * Dependencias: otros productos de desarrollo de los que depende el requisito. Es el concepto más habitual de trazabilidad, en el que se atribuyen los requisitos con la información de otros productos de desarrollo que, en caso de cambio, podrían tener impacto sobre el requisito. Esta información es fundamental para poder realizar un análisis de impacto de un cambio dentro del Procedimiento de control de cambios establecido en el proyecto.

La información de las dependencias no siempre se muestra asociada a cada requisito, sino que es habitual representarla en forma de matriz de trazabilidad o de listas de trazabilidad.

*Importancia*: La importancia de un requisito indica la relevancia del requisito para los clientes y usuarios, y suele estar relacionada con la importancia de los objetivos de negocio que el requisito ayuda a cumplir. La importancia se suele expresar de diversas formas:

    * Valores numéricos: se asigna un valor numérico a la importancia del requisito, normalmente entre 0 y 3 o entre 0 y 5. Algunas propuestas asumen que el valor mínimo (cero o uno normalmente) es la máxima importancia, mientras que otras asumen que es el valor máximo el que representa la importancia.
    * Valores enumerados: se crea una escala de prioridad con valores como alta, media y baja. También se pueden usar una escala ordinal con literales con expresiones como vital, importante y prescindible y se asigna a cada requisito un valor. Puede existir una correspondencia directa con valores numéricos (por ejemplo alta = 0, media = 1 y baja = 2).

*Estabilidad*: La estabilidad de un requisito indica una estimación de la probabilidad de que el requisito no cambie durante el resto del desarrollo. Este atributo es especialmente interesante para detectar posibles fuentes de cambios en un proyecto y prepararse para ello. Puede expresarse como un valor numérico (como un porcentaje de probabilidad por ejemplo) o como un valor enumerado (por ejemplo: alta, media o baja).

*Comentarios*: Es conveniente dejar abierta la posibilidad de atribuir los requisitos con alguna otra información no prevista inicialmente. Algunas herramientas de gestión de requisitos permiten definir nuevos atributos de requisitos de forma dinámica. Si no se dispone de esta posibilidad, se debe recurrir a atribuirlos con los comentarios que se crea oportuno. De hecho, algunas herramientas de gestión de requisitos no sólo permiten comentarios, sino que incorporan funcionalidades similares a los foros para que se puedan desarrollar discusiones sobre los requisitos.

Actividades y su descripción
============================

*Recolección*: Recolección y documentación de requisitos es una actividad de comunicación iterativa entre clientes, gerentes y practicantes, para descubrir, definir, refinar y registrar una representación precisa de los requisitos del producto. Varios métodos son utilizados para la recolección de requisitos. Algunos análisis iniciales como es la agrupación, categorización, priorización son desarrollados durante esta actividad.

*Documentación*: Después que los requisitos han sido recolectados, hay que analizarlos a detalle y documentarlos en una especificación de requisitos. El resultado de la especificación de requisitos y de cualquier especificación de requisitos de componentes hardware/software derivado sirve como registro de convenio con el cliente y compromiso con el proveedor. Estas especificaciones son rastreadas utilizando una matriz de trazabilidad de requerimientos y son sujetos a verificación y gestión de cambio a través del ciclo de vida del producto.

*Verificación*: Una vez que la especificación de requisitos ha sido desarrollada, los requisitos son verificados. La verificación de requisitos es un proceso para asegurar que la especificación de requisito del producto es una representación exacta de las necesidades del cliente. Este proceso también asegura que los requisitos sean trazados y verificados a través de varias fases del ciclo de vida; particularmente en el diseño, implementación y pruebas. Además, todos estos requerimientos deben ser trazados al diseño, implementación y pruebas para asegurarse que los requerimientos han sido satisfechos.

*Gestión de Cambios*: Gestión de cambios es un proceso formal para identificar, evaluar, trazar y reportar cambios propuestos y aprobados a la especificación del producto. Como el proyecto va evolucionando, los requerimientos pueden cambiar o expandirse para ajustar algunas modificaciones en el alcance o diseño del proyecto. Un proceso de gestión de cambios proporciona un rastreo completo y preciso de todos los cambios que son pertinentes al proyecto. El proceso del ciclo de vida de la Gestión de Requisitos, debe ser flexible y adaptable para reunir las necesidades del proyecto. Las características del alcance e implementación del proceso del ciclo de vida de la Gestión de Requisitos en un proyecto, variará dependiendo de algunos factores claves.

* Tamaño y complejidad del proyecto
* Experiencia del personal del proyecto
* Experiencia de los clientes del proyecto
* Dominio de la aplicación
* El propósito y uso de esta aplicación

Verificación de requerimientos
==============================

Se verifica que tanto los requerimientos como la documentación cumplan con los estándares definidos. El estándar de formalización de los requerimientos es la Especificación de Requerimientos, por lo que se revisará el apego a este estándar. Se revisará que no haya incongruencias. Se prestará especial énfasis a los requerimientos versus la especificación formal de ese requerimiento específico. Se verificará que todo requerimiento esté contemplado a través de algún punto en la especificación y que todo punto en la especificación satisfaga algún requerimiento. 

Buenas prácticas en la Gestión de Requisitos
============================================

* Priorizar requisitos: para determinar aquellos que se deberían cumplir en la primera versión o producto y aquellos que pueden llevarse a cabo en sucesivas versiones.
* Establecer líneas base de los requisitos: para asegurar que cualquier modificación en los requisitos que cambie la línea base se trate como cambios de alcance.
* Comunicación abierta: para asegurar que la información relacionada con los requisitos se comunica de forma consistente. Una comunicación abierta también implica comunicar a la gente correcta y al conjunto mínimo de personas. 
* Gestión de cambios de los requisitos: es esencial gestionar estos cambios de forma efectiva y eficiente.
* Mantener trazabilidad de requisitos: para llevar un seguimiento de la vida de un requisito.
* Establecer un plan de mejora de procesos para la ingeniería de requisitos: para cumplir con las necesidades actuales y futuras de forma más eficiente y con mayor calidad.
* Formar a los analistas de requisitos: para asegurar que los analistas de requisitos tienen el conocimiento, entre otros aspectos, de cómo escribir buenos requisitos, etc.
* Los requerimientos deben de ser completos, consistentes y objetivos, así como testeables y viables en su realización.
* Utilizar un modelo estructural en la captura de información y usar técnicas de obtención de requisitos en el trato con el cliente.
* Formar a los analistas de requisitos en el ámbito de la información a analizar.
* Mantener viva la documentación de requisitos y su trazabilidad.
* Utilización de herramientas específicas para la gestión de requisitos.

Métricas Sugeridas
==================

A fin de valorar la calidad del modelo de análisis y la correspondiente especificación de requisitos, se sugiere que el equipo tenga en cuenta las métricas que establece David. Dichas métricas son detalladas a continuación:

* Para determinar la especificidad de los requisitos, se sugiere una métrica basada en la consistencia de la interpretación de los revisores para cada requisito:
		
    Q1 = nui / nr
	
    Donde nui es el número de requisitos para los que todos los revisores tuvieron interpretaciones idénticas. Cuanto más cerca de uno este el valor de Q1 menor será la ambigüedad de la especificación.

* Para la corrección de requisitos, se sugiere una métrica que indique la proporción de requisitos correctos (verificados): 

    Qc = Nc / (Nc + Nnv)

    Nc: cant. requisitos correctos y Nnv: cant. Requisitos aún no verificados 

* Para determinar que tan concisa es una especificación, sin desmejorar su calidad global, se sugiere la siguiente métrica 
    
    Qs = 1 / (Size +1) 

    Size: cantidad de páginas de la especificación. Un valor apropiado puede ser 0.1. 

* Para determinar la comprensibilidad de los requisitos, es decir, si el significado de los requisitos son entendidos por todos los usuarios e interesados, se sugiere la siguiente métrica:
    
    Qu = Nru / Nr 
    
    Nru: cant. requisitos comprendidos por “todos” los interesados.
    Nr: cantidad de requisitos totales, tanto funcionales como no funcionales.

Herramientas
============

Las herramientas que los gestores de requisitos utilizan para automatizar los procesos de Ingeniería de Requisitos, han disminuido el trabajo duro en el mantenimiento de requisitos, añadiendo beneficios importantes al reducir errores. Estas herramientas también ayudan a evaluar el posible impacto de los cambios en los requisitos, en los procedimientos, costes y personal.
Mientras mayor flexibilidad tenga la herramienta, mucha mayor posibilidad de ajustarse a las necesidades que se tienen.
Se enuncian algunas herramientas comunes:

* IRqA: es una herramienta de ingeniería de requisitos especialmente diseñada para soportar el proceso completo de ingeniería de requisitos. En IRqA el ciclo de especificación completo incluye la captura de requisitos, análisis, especificación de sistema, validación y la organización de requisitos es soportada por modelos estándares
* Doors: a diferencia del resto de las herramientas, considera los requisitos como objetos y los documentos como módulos. Tiene una orientación basada en objetos. Es una herramienta para organizaciones grandes que necesitan controlar complejos conjuntos de usuarios y requisitos de sistemas con una completa trazabilidad. Proporciona buena visualización de tales documentos como jerárquicas, y su lenguaje de extensión permite una gran variedad de soporte de herramientas a ser construidas.
* RequisitePro: es una herramienta centrada en documentos, que almacena los requisitos asociandolos a documentos. Auxilia especialmente en el control de cambio de requisitos, con trazabilidad para especificaciones de software y pruebas.