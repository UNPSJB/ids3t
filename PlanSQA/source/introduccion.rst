.. include:: global.rst

.. _introduccion:

************
Introducción
************

Una de las principales fases dentro de la elaboración de un proyecto es el Aseguramiento de la Calidad del Software (SQA), es decir, un modelo sistemático y planeado de todas las acciones necesarias para proveer la confianza adecuada, según los requerimientos técnicos establecidos, de cada producto e ítem del proyecto. Un sinónimo del aseguramiento de la calidad del software es aseguramiento del producto de software.

El plan de aseguramiento de la calidad del software (SQAP) define cuan adherido a estos estándares se debe monitorear. El SQAP contiene una lista de comprobación para las actividades que se deben llevar a cabo para asegurar la calidad del producto. Para cada actividad, en las que tiene responsabilidad el SQA, se debe crear un plan para su monitoreo.

En este documento se describen todos los planes y roles que tendrá cada elemento de la organización en el proceso de aseguramiento de la calidad del software.

Propósito
=========

La definición de este Plan de SQA, tendrá como propósito servir como soporte para el desarrollo de un producto de alta calidad, definiendo las actividades mínimas que deben realizar los involucrados para alcanzar dicho objetivo.

Los elementos que son alcanzados por el Plan comprende a:

* Especificación Formal de los Requerimientos.
* Modelos de Diseño.
* Código y Tests generados.
* Documentación desarrollada.

El siguiente Plan cubre las etapas del Proceso vinculadas con la Ingeniería de Requerimientos, Diseño, Implementación, Pruebas. Además, se definirán las acciones a tener en cuenta en la Gestión de la Configuración del Software y en la Gestión de Riesgos.

Roles y tareas SQA
==================

El responsable de SQA tiene la libertad de reportar anomalías y no conformidades (si la calidad del producto está en peligro), al siguiente o al nivel más alto en la cadena de liderazgo en la organización del proyecto. 

**Administrador SQA, es responsable de lo siguiente:**

* Establecer un programa de calidad para el proyecto.
* Identificar las actividades de SQA que se llevarán a cabo.
* Resolver problemas relacionados con la calidad.
* Auditar y reportar las funciones SQA para este proyecto.
* Monitorear el cumplimiento de las actividades planificadas en el plan de SQA
* Garantizar la calidad de los entregables, la documentación y de los procesos utilizados para producir software. 

**Gerente Técnico Responsable de:**

* Establecer un programa de calidad para cada proyecto de desarrollo de software de  acuerdo a las políticas organizacionales.
* Revisar y aprobar el plan de SQA para cada proyecto.
* Monitorear las actividades de SQA.
* Resolver cualquier conflicto relacionado con las actividades de SQA.
* Identificar un grupo independiente para la auditoría de las actividades de SQA de ser preciso.

**Jefe de Proyecto Debe:**

* Establecer un programa de calidad para el proyecto de desarrollo de software de acuerdo a las políticas organizacionales.
* Identificar las actividades de SQA requeridas para el proyecto.
* Revisar y aprobar el plan de SQA para el proyecto.
* Identificar los participantes de las actividades de SQA.
* Implementar las actividades de SQA de acuerdo al plan.
* Monitorear las actividades de SQA planificadas en el plan.
* Identificar los factores de calidad para la implementación del software.
* Identificar, desarrollar y mantener la documentación del proyecto.

**Pruebas es responsable de:**

* Comentar acerca del plan de SQA.
* Implementar la calidad en las pruebas de acuerdo al plan SQA.
* Resolver y dar seguimiento a cualquier asunto de calidad que tenga relación con las pruebas del sistema.
* Verificar que los factores de calidad se implementaron en el sistema.
* Implementar las prácticas de pruebas en el sistema, procesos y procedimientos, como está definido en el documento de pruebas.

** Diseño y codificación son responsables de:**

* Comentar acerca del plan de SQA.
* Implementar la calidad en el diseño y codificación de acuerdo a este plan de SQA.
* Resolver y dar seguimiento a cualquier asunto de calidad que tenga relación con el diseño del sistema, arquitectura del sistema y desarrollo del mismo.
* Identificar, implementar y evaluar los factores de calidad que van a ser implementados en el sistema.
* Implementar el diseño, arquitectura, desarrollo, procesos y procedimientos necesarios para el sistema, siguiendo los documentos de planeación para cada uno de estos.

**Administración de riesgos es responsable de:**

* Dar seguimiento a los riesgos identificados.
* Buscar medidas de contingencia de los riesgos identificados. 
* Comentar acerca del plan de aseguramiento de la calidad.
* Notificar al administrador del proyecto cuando un riesgo identificado, se convierta en un problema.

**Administrador de requerimientos:**

* Realizar el ERS.
* Comentar acerca del plan de aseguramiento de la calidad.
* Implementar calidad en el ERS.
* Analizar los requerimientos.

**Métricas es responsable de:**

* Realizar el plan de Métricas para el proyecto.
* Evaluar las métricas recabadas a lo largo del proyecto.
* Comentar acerca del plan de aseguramiento de la calidad.
* Implementar la calidad en el plan de métricas del proyecto.

**SCM (Administrador de Configuración) es responsable de:**

* Revisar y comentar el plan de SQA para el proyecto.
* Implementar las actividades de calidad de acuerdo al plan de SQA.
* Resolver los problemas detectados por SQA relacionados con SCM.
* Implementar las prácticas, procesos y procedimientos definidos en el plan de SCM y en otros planes o documentos complementarios.

+------------------------+-----------+----------------+-----------------------+-------------------+------------+----------+-----+
| **Plan SQA**           | Admin SQA | Admin Proyecto | Adm. de Configuración | Desarrollo/Diseño | Pruebas SW | Plan SQA | Req |
+========================+===========+================+=======================+===================+============+==========+=====+
| Desarrollar /          |  X        |    X           |                       |                   |            |          |     |
| Documentar el Plan SQA |           |                |                       |                   |            |          |     |
+------------------------+-----------+----------------+-----------------------+-------------------+------------+----------+-----+
| Revisar el Plan SQA    | X         | X              | X                     | X                 | X          | X        | X   |
+------------------------+-----------+----------------+-----------------------+-------------------+------------+----------+-----+
| Aprobar el Plan SQA    | X         | X              |                       |                   |            |          |     |
+------------------------+-----------+----------------+-----------------------+-------------------+------------+----------+-----+
