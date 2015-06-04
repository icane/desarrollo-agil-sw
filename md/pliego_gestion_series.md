Desarrollo de un sistema integral de gestión de actualizaciones y series estadísticas
=====================================================================================

-----------------------------------------------------------------
Resumen de características
-----------------------------------------------------------------
- Centro destinatario: Instituto Cántabro de Estadística (ICANE).
- Presupuesto formulado por la administración: 17.990 € + IVA.
- Distribución por anualidades:
- 2015: 17.990 € + IVA.
- Plazo de ejecución: 20 semanas.
-----------------------------------------------------------------

Objeto del contrato
-------------------
Acometer la ejecución del proyecto **Desarrollo de un sistema integral de gestión de actualizaciones y series estadísticas** para el Instituto Cántabro de Estadística (ICANE).

###Información general
Con el objeto de servir de la forma más idónea posible a las necesidades de información que demandan los agentes que componen la realidad social y económica de Cantabria, el ICANE, siguiendo el *código de buenas prácticas en las estadísticas europeas adoptado por el Comité del Programa Estadístico el 24 de febrero de 2005*[COD00], se acoge a los principios de independencia profesional, mandato relativo a la recogida de datos, idoneidad de los recursos, compromiso con la calidad, secreto estadístico e imparcialidad y objetividad. El cuarto principio de dicho código de buenas prácticas afirma que todos los miembros del Sistema estadístico europeo (SEE) se **comprometen a trabajar y cooperar** conforme a los principios establecidos en la Declaración sobre la **calidad del Sistema estadístico europeo**.

En este contexto y en el de la situación tecnológica en materia de tratamiento y difusión de datos estadísticos en que se encuentra el ICANE, se hace necesario **mejorar los procesos, mecanismos y controles que permiten garantizar y asegurar la publicación y difusión de dichos datos con la calidad que se espera de un organismo de estas características**. Es por ello que con este proyecto se pretende consolidar una forma de trabajo conforme con los recursos técnicos y humanos existentes en el ICANE que permita garantizar la difusión de datos estadísticos con agilidad y calidad de manera sostenida en el tiempo.

###Necesidades
- Reducción del tiempo global de realización de actualización de datos y desarrollo de nuevas series estadísticas para su difusión.
- Reducción o práctica eliminación de errores en la difusión de datos en entorno de producción.
- Reducción de la curva de aprendizaje de los distintos procedimientos de actualización y carga de datos.

###Metas a alcanzar
- Industrialización de los flujos de trabajo diarios de la operativa de actualización de datos.
- Automatización de los procesos de despliegue de modificaciones y nuevas series en entornos de desarrollo, pruebas y producción.
- Automatización de la generación de estructuras OLAP a partir de metadatos.
- Automatización de la creación de series estadísticas simples basadas en archivos PC-Axis.

Descripción de la situación actual
----------------------------------
[Ver presentación on-line.](http://slides-icane.rhcloud.com/series.html)

Descripción y requisitos del sistema
------------------------------------
###Requisitos funcionales
Ver anexo requisitos funcionales.

###Historias de usuario
Ver anexo de historias de usuario.

###Requisitos de interfaz, diseño gráfico, formato y estilo
Ver anexo de requisitos de interfaz, formato y estilo.

###Volúmenes de información y expectativas de crecimiento.
El adjudicatario propondrá los parámetros de dimensionamiento inicial del sistema, tanto a nivel hardware como software, debiendo tener en cuenta su previsión de crecimiento. En todo momento se tendrán en cuenta los recursos proporcionados por la infraestructura tecnológica del ICANE.

###Requisitos de integración con otros sistemas y migración
Ver anexos de requisitos de integración y migración.

###Requisitos de rendimiento
Ver anexos de requisitos de rendimiento.

### Atributos de calidad
Ver anexo de requisitos de calidad.

###Requisitos de funcionamiento del sistema
Ver anexo de requisitos de funcionamiento.

###Requisitos de accesibilidad
Ver anexo de requisitos de accesibilidad.

###Requisitos de seguridad
Ver anexo de requisitos de seguridad.

###Formación
- Se establecerá un plan de formación adecuado y suficiente sobre la utilización del sistema, integrando la documentación electrónica asociada en la infraestructura del ICANE.
- El número de personas a formar será determinado por el ICANE, y su perfil será el de usuario informático avanzado (nivel medio/alto).
- La formación tendrá lugar en las instalaciones de la sede del ICANE en Santander, Hernán Cortés 9, 1ª planta.

Entornos de desarrollo, pruebas y explotación
---------------------------------------------
Los técnicos del ICANE proveerán al adjudicatario de las máquinas virtuales necesarias según las propuestas de este último.

###Entorno físico
- HP c3000: Chasis c3000 para ProLiant BL cClass monofásico.
- HP ProLiant BL460c: Xeon Dual Core E5150 (2.66 GHz/ 1x4MB caché/ 1333 FSB), 8 GB RAM DDR2667, Disco SAS SFF de 146GB 2.5.
- HP ProLiant BL460c: Xeon Quad Core E5420 (2.50 GHz/ 1x4MB caché/ 1333 FSB), 8 GB RAM DDR2667, Disco SAS SFF de 146GB 2.5.
- HP VC-Enet Module: 1/10Gb.
- HP MSA 2012i: cabina iSCSI con 8 discos SAS 300GB en dos LUNs con RAID5.

###Entorno virtual
- Hypervisor: RHEV Hypervisor 5.8.
- Manager: RHEV Manager 2.2.9.52985.
- Estructura:
 - 1 datacenter: ICANE.
 - 1 cluster: Producción.
 - 4 hosts: bladesrv1, bladesrv2, bladesrv3, bladesrv4.
 - 2 dominios de almacenamiento de 900 GB cada uno: Avalon y Camelot.
 - 23 VMs corriendo en la actualidad.
 - 1 plantilla de Debian 7.7.

###Entorno de red
Todos los sistemas y servidores serán desplegados en la red LAN técnica del ICANE, siendo ésta una red Ethernet 100Mbps/1Gbps basada en TCP/IP. Dicha red está comunicada con la LAN del ICANE y la red de Gobierno de Cantabria a través de sendos cortafuegos, de cuya gestión se hace cargo el Gobierno de Cantabria.

###Entorno de desarrollo
El adjudicatario propondrá una arquitectura lógica para el entorno de desarrollo basada en la existente actualmente, compuesta por cuatro máquinas virtuales idénticas que cuentan con un despliegue del banco de datos en su rama de desarrollo y conexión a una base de datos común. Dicha arquitectura deberá ser aceptada por los técnicos del ICANE/DGOT. Para documentar dicha propuesta se utilizará un diagrama de despliegue bajo el estándar UML 2.0[FOWLER00].

###Entorno de pruebas
El adjudicatario propondrá una arquitectura lógica para el entorno de pruebas basada en la existente actualmente, compuesta por una máquina virtual que cuenta con un despliegue del portal web del ICANE con licencia de desarrollo y un despliegue del banco de datos en su rama de pruebas así como una máquina virtual con un despliegue del sistema de metadatos en pruebas. Dicha arquitectura deberá ser aceptada por los técnicos del ICANE/DGOT. Para documentar dicha propuesta se utilizará un diagrama de despliegue bajo el estándar UML 2.0.

###Entorno de explotación
El adjudicatario propondrá una arquitectura lógica de despliegue del sistema, que deberá ser aceptada por los técnicos del ICANE/DGOT. Para documentar dicha propuesta se utilizará un diagrama de despliegue bajo el estándar UML 2.0.

Ejecución y gestión del proyecto
--------------------------------
###Planificación
El proyecto tendrá una duración máxima de 20 semanas.

La planificación de los trabajos se realizará en ciclos o sprints de 15 días, decidiéndose en las correspondientes reuniones el número de características a implementar durante el siguiente ciclo en función de su coste estimado, que se irá concretando con menor incertidumbre a medida que transcurran las distintas iteraciones. Dicho coste se volverá a estimar conjuntamente entre el adjudicatario y el equipo técnico de ICANE, siguiendo la técnica de *planning poker*.

La planificación deberá realizarse teniendo en cuenta las fases incluidas en el apartado *“Fases del desarrollo“*.

###Dirección
El ICANE designará un equipo representativo no mayor de tres personas para el papel de cliente o *product owner*.

El adjudicatario proporcionará el equipo de desarrollo que trabajará conjuntamente con el equipo técnico del ICANE y un facilitador o  *scrum master*, que desempeñará las funciones propias de este rol además de participar activamente en el desarrollo y construcción de la aplicación.

Corresponde al ICANE la supervisión, control y aprobación de los trabajos, así como determinar las correcciones que se estimen oportunas.

###Equipo de trabajo
La jornada de trabajo será de lunes a viernes, de acuerdo con el horario que se establezca con el ICANE.  No obstante, en circunstancias excepcionales y **cuando a criterio del ICANE la realización efectiva de los trabajos no se ajuste a la planificación, el adjudicatario deberá comprometerse a  una plena disponibilidad**.

El equipo de trabajo estará formado por:

- El equipo de desarrollo del adjudicatario, en el que se incluye un facilitador *scrum master*.
- El cliente o *product owner*, formado por dos Técnicos de Estadísticas Económicas o Socio-demográficas y el Jefe de Sección de Informática Estadística y Banco de datos.
- El área de informática del ICANE cuando así se requiera.

###Seguimiento y control
El seguimiento y control del proyecto se efectuará sobre las siguientes bases:

- Reuniones cada 15 días del equipo de trabajo: *Sprint Planning Meetings* y *Sprint Review Meetings + Retrospective*, donde se planificará la iteración siguiente y se revisará la anterior.
- Reuniones diarias entre el equipo de desarrollo del adjudicatario y el cliente, de no más de 15 minutos (*Daily Scrum*). Dichas reuniones podrán ser presenciales o en modalidad *on-line*, a través de una herramienta de colaboración o mensajería a determinar por parte del equipo de trabajo.
- Tras las revisiones técnicas, el ICANE podrá rechazar en todo o en parte los trabajos realizados, en la medida que no respondan a lo acordado o que no superasen los controles de calidad o pruebas de aceptación previstos.
- El proyecto se ejecutará en iteraciones incrementales con una demostración del producto al finalizar cada iteración.
- Los requisitos se desarrollarán priorizados por el valor aportado al ICANE (definido este por el equipo de trabajo), de modo que en las primeras iteraciones se consigan los objetivos más importantes del proyecto y se puedan realizar ajustes al respecto con la suficiente antelación.
- El control y seguimiento del proyecto se basará en los requisitos completados en cada iteración. Se entenderá un requisito como completado si incluye todos los entregables asociados realizados (documentación, pruebas, código fuente, etc.); dichos entregables se decidirán en cada iteración por parte del equipo de trabajo.
- La medición del progreso del proyecto se realizará a través de un gráfico *BurnDown*.

###Productos que se deben obtener
Los productos resultantes de la ejecución del contrato, que deben por tanto ser entregados conforme a lo expresado en el presente pliego son:

####Código fuente
Se entregará la última versión libre de errores del código fuente de los desarrollos a medida y cualquier librería o componente abierto que haya sido objeto de modificación. Dicho código fuente se encontrará en un repositorio de un sistema de control de versiones a decidir por parte del equipo de trabajo, que será accesible en todo momento por adjudicatario e ICANE, siendo propiedad de este último.

####Documentos
Los documentos a entregar con el desarrollo de cada característica se decidirán en las correspondientes reuniones de sprint. Entre dichos documentos podrá haber:

- Diagramas de clases UML que faciliten la comprensión y comunicación de las partes más complejas del sistema.
- Diagramas de despliegue UML para cada uno de los entornos.
- Diagramas de componentes UML que faciliten la comprensión y la comunicación de la arquitectura final del sistema.
- Cualquier otro informe o diagrama que se considere de interés por parte del equipo de trabajo según la evolución del proyecto, acordándose en la iteración correspondiente.
- Memoria fin de proyecto con, al menos, los siguientes apartados:
 - Situación de partida.
 - Necesidades.
 - Alcance efectivo de los trabajos realizados con detalle de entregables.
 - Recursos consumidos.
 - Objetivos e hitos conseguidos.
 - Propuesta de recomendaciones de actividades.
 - Situación final.
 - Resumen de las ofertas técnica y económica.

####Sistema funcional y tareas de construcción
El adjudicatario será responsable de entregar aquellos scripts y/o tareas necesarios para construir y desplegar el software desarrollado en la infraestructura TIC del ICANE, proporcionando soporte en la puesta en marcha del mismo, que será llevada a cabo por los técnicos del ICANE/DGOT.

Los técnicos del ICANE deben de ser capaces de construir y desplegar el sistema completo en los distintos entornos de desarrollo, pruebas y producción, así como ejecutar los tests que en cada caso se definan (unitarios, integración, funcionales...).

####Plataformas y lugar de trabajo
- Los trabajos se realizarán normalmente en las dependencias del adjudicatario o en las  instalaciones en la sede del ICANE, según se acuerde, autorice y determine.
- El ICANE/DGOT pondrá a disposición del adjudicatario su plataforma de infraestructura virtual para desplegar el producto tanto en entornos de prueba como de explotación.
- El adjudicatario deberá proporcionar el producto de forma temporal en las instalaciones e infraestructura del ICANE/DGOT, o bien un acceso remoto al mismo, para llevar a cabo las sesiones de control que así lo requieran (pruebas, selección de prototipos, etc.).
- El adjudicatario utilizará sus propias licencias de uso de las herramientas de desarrollo para el proyecto, en caso de ser necesarias, **procurando en todo caso utilizar software de fuentes abiertas**.

Presupuesto de licitación y forma de pago
-----------------------------------------
La cuantía máxima de contratación se desglosa de la forma siguiente:

- Presupuesto base: 17.990,00 €.
- IVA: 3.777,90 €.
- Presupuesto total: 21.767,90 €.

El pago del contrato se efectuará una vez aceptada la totalidad de los trabajos mediante transferencia bancaria.

Propiedad intelectual, confidencialidad y privacidad
-----------------------------------------------------
###Propiedad intelectual de los trabajos
El contratista acepta expresamente que los derechos de explotación del sistema de información así como de cualquier programa o código desarrollado específicamente al amparo del presente contrato corresponden únicamente al ICANE con exclusividad y a todos los efectos, pudiendo (el ICANE) reproducirlos o divulgarlos total o parcialmente. Se garantizará que todo el software y las herramientas utilizadas no vulneran ninguna normativa, contrato, derecho, interés o propiedad de terceros.

###Confidencialidad de la información
El adjudicatario queda expresamente obligado a mantener absoluta confidencialidad y reserva sobre cualquier dato que pudiera conocer con ocasión del cumplimiento del contrato, especialmente los de carácter personal, que no podrá copiar o utilizar con fin distinto al que figura en este pliego, ni tampoco ceder a otros ni siquiera a efectos de conservación.

El adjudicatario no podrá utilizar los datos a los que tenga acceso en la ejecución de este contrato para otro fin distinto al estipulado en el mismo, ni los comunicará a otras personas.

###Privacidad y protección de datos.
Será de exigido cumplimiento la normativa vigente en materia de protección de datos de carácter personal (Ley Orgánica 15/1999 de 13 de diciembre de Protección de Datos de Carácter Personal, LOPD, y Real Decreto 1720/2007, de 21 de diciembre, por el que se aprueba el Reglamento de desarrollo de la Ley Orgánica 15/1999, de 13 de diciembre, de protección de datos de carácter personal), en todos aquellos ficheros que tengan relación con el proyecto y contengan datos de carácter personal en los que sea de aplicación y con los niveles de seguridad que corresponda.

El adjudicatario deberá adoptar las medidas de seguridad precisas de tipo físico, lógico y técnico-administrativo que garanticen la seguridad, disponibilidad, confidencialidad e integridad de los datos y programas manejados así como de la documentación facilitada y las instalaciones.

Metodología en la elaboración de los trabajos
---------------------------------------------
###Metodología de desarrollo
Para el desarrollo del sistema objeto del presente contrato se utilizarán metodologías y prácticas Ágiles[BOB00]: Scrum, Kanban y XP[BECK00]. Se decidirá por parte del equipo de trabajo si es adecuado utilizar alguna herramienta de gestión *on-line*, siendo seta de carácter abierto, gratuito o proporcionada por el adjudicatario.

Se planificarán sprints de dos semanas de duración desde el inicio del proyecto, con reuniones entre el adjudicatario, los técnicos del ICANE/DGOT y los usuarios responsables del proyecto cada 15 días. La planificación de dichas reuniones podrá ser modificada a conveniencia del equipo de desarrollo siempre y cuando exista consenso mayoritario.

El ICANE podrá **añadir, eliminar o modificar los requisitos del sistema sin coste adicional** por criterio propio o siguiendo las recomendaciones del adjudicatario siempre y cuando el esfuerzo **total estimado resultante no supere en un 15% al estimado inicialmente por el adjudicatario**. En caso de llegar a este límite, los requisitos aún podrán ser modificados o añadidos en detrimento de otros. A estos efectos, **no se considerarán cambios las subsanaciones por parte del adjudicatario de los defectos de calidad del producto** propuestos por el equipo técnico o por él mismo.

Los requisitos podrán y serán revisados, modificados, ampliados y detallados en cualquier reunión de cualquier sprint, a petición tanto del adjudicatario como de los técnicos del ICANE/DGOT, debiendo contar con la aprobación final de estos últimos y quedando sujetos, en todo caso, a lo expuesto en el párrafo anterior.

Asimismo, en cada iteración se ajustarán las estimaciones realizadas conforme se vaya disponiendo de la información suficiente como para reducir al máximo cualquier tipo de incertidumbre. Todas aquellas desviaciones por exceso con respecto a las estimaciones iniciales atribuibles al adjudicatario correrán a su riesgo y ventura. Del mismo modo, las desviaciones por defecto con respecto a las estimaciones iniciales se transformarán en esfuerzo asignado a la implementación de funcionalidad u otras características de nueva necesidad surgidas a lo largo del desarrollo del proyecto a decidir por los técnicos del ICANE/DGOT.

###Fases del desarrollo
####Iteración 0 – Verificación de la lista de objetivos/requisitos y planificación
- Duración: Dos semanas.
- Objetivos: Planificar y distribuir los objetivos y alcance del proyecto en iteraciones, de manera que los requisitos estén priorizados balanceando el beneficio que aportan al ICANE, su coste de desarrollo y los riesgos del proyecto.
- Actividades:
 - Priorización de los requisitos en iteraciones y entregas y definición del *product backlog* considerando los siguientes criterios:
   - El valor aportado por cada requisito para el ICANE.
   - El esfuerzo necesario para desarrollar cada uno de los requisitos, de manera que en las primeras iteraciones se desarrollen los requisitos que proporcionen el máximo valor con el mínimo esfuerzo y que puedan encajar en la periodicidad de las iteraciones.
   - Las dependencias inevitables entre requisitos.
   - Minimizar los riesgos del proyecto respecto a desarrollo de los requisitos, disponibilidad y grado de implicación de los actores y beneficiarios participantes, interacción con otros equipos, etc.
   - Maximizar la cohesión del contenido de cada iteración, identificando los puntos de acoplamiento y las dependencias entre los diferentes incrementos de manera que sean mínimos, para poder dar por realmente completados los requisitos desarrollados en cada una de las iteraciones.
 - Calcular la duración de cada uno de los incrementos desarrollados de manera que puedan encajar en la periodicidad de las iteraciones.

####Iteraciones de desarrollo
- Duración: dos semanas cada iteración.
- Objetivos: Completar un incremento de producto que sea demostrable al finalizar la iteración.
- Actividades:
 - En el inicio de cada iteración:
   - El ICANE y el adjudicatario mantendrán una reunión para consensuar los objetivos y contenido de la iteración en función de los criterios de priorización indicados anteriormente, así como para dar detalle a los requisitos seleccionados (sprint backlog) en forma de desglose de tareas, en la medida en que cada una de las dos partes necesiten. De manera general, cada requisito deberá tener asociado un conjunto de condiciones o pruebas de aceptación para poder considerar que el requisito ha sido completado.
   - Al utilizarse un enfoque iterativo e incremental, en la implementación de cada característica se llevarán a cabo las distintas fases de un desarrollo de software tradicional (análisis, diseño, construcción y pruebas).
 - Al finalizar cada iteración:
   - El adjudicatario deberá realizar una demostración de los requisitos o historias de usuario completados. En esta demostración participará el equipo de trabajo al completo. El ICANE confirmará la aceptación de estos requisitos realizando las comprobaciones de calidad oportunas.
   - Los tests implementados deberán satisfacer las pruebas de aceptación definidas en la reunión del comienzo del sprint. Tras analizar las características desarrolladas, el equipo de trabajo decidirá si es necesaria una refactorización[FOWLER01] de las mismas, debiendo llevarse a cabo por el adjudicatario en el siguiente sprint en caso de ser necesario.
   - El ICANE podrá volver a priorizar el conjunto de requisitos del proyecto y consensuará con  el adjudicatario el contenido de las siguientes iteraciones según lo estipulado en el apartado *Metodología del desarrollo* de este pliego. En particular, los elementos a volver a priorizar podrán ser: requisitos inicialmente identificados del proyecto, modificaciones a estos requisitos, nuevos requisitos que aparezcan durante el proyecto, problemas de calidad detectados, etc.
- Entregables:
El producto desarrollado hasta ese momento incluyendo todos los entregables asociados completados (documentación, etc.) e integrados a su vez con los entregables de las iteraciones anteriores, de manera que dicho producto sea susceptible de ser entregado con el mínimo esfuerzo en ese mismo momento.

###Software de base y estándares
Para el desarrollo de las actividades definidas en el presente Pliego Técnico, habrá de tenerse en cuenta el empleo de los estándares tecnológicos adoptados por el ICANE (de cumplimiento cuando proceda según las necesidades del proyecto y siempre que no entren en conflicto entre sí):

- Entorno tecnológico: Java SE, Java EE o compatibles.
- Frameworks de desarrollo: frameworks de desarrollo ágil compatibles con el entorno (ej: **Grails**).
- Metodologías y prácticas ágiles: Scrum, **Extreme Programming**, Lean IT, Kanban.
- Entorno integrado de desarrollo: **vim + tmux + zsh**, Eclipse IDE o derivados.
- Bases de datos: SQL (MySQL/MariaDB), XML(**eXist**).
- OLAP: MDX, XMLA, Mondrian.
- Red: TCP/IPv4, HTTP, HTTPS.
- Sindicación de noticias: RSS.
- Contenido: HTML5, XHTML, XML.
- Tecnologías WUI: JQuery, AJAX, CSS3 y librerías derivadas.
- Documentos: PDF, CSV, OpenDocument, formatos de Microsoft Office 2003 y anteriores (DOC, XLS, etc.), formatos de Microsoft Office 2007 -Office Open XML- (DOCX, XLSX, etc.), **Markdown**, **UML 2.0**, etc.
- Imágenes: PNG, SVG y demás estándares comúnmente aceptados en el mercado.
- Archivos comprimidos: ZIP, TGZ.
- Servicios web restful, JSON, XML, JAX-RS.
- Despliegue de aplicaciones: contenedores Tomcat o derivados
- Gestión de ciclo de vida y dependencias software: Ant, Maven, Gradle.
- Integración continua: Jenkins.
- Otros: en general, cualquier estándar propuesto por los técnicos del ICANE/DGOT que proporcione independencia de proveedores y licenciamiento.

Toda la documentación, diagramas adjuntos, etc. deberá construirse en forma de artefactos cuya fuente consista en archivos de texto planos.

Garantía de los trabajos
------------------------
###Condiciones generales
El adjudicatario deberá garantizar por un mínimo de un año los productos derivados de la presente contratación, a contar desde la fecha de recepción de los mismos, obligándose a realizar durante dicho período los cambios necesarios para solventar las deficiencias detectadas imputables a la firma adjudicataria si así lo solicita el centro directivo.

Dicha garantía incluirá la subsanación de errores o fallos ocultos que se pongan de manifiesto en el funcionamiento de los desarrollos, o que se descubran mediante pruebas o cualesquiera otros medios, así como la conclusión de la documentación incompleta y subsanación de la que contenga deficiencias. Los productos originados como consecuencia de la subsanación de fallos deberán entregarse de conformidad con lo exigido en este pliego.

Transferencia tecnológica y documentación
-----------------------------------------
Durante la ejecución de los trabajos objeto del contrato el adjudicatario  se compromete, en todo momento, a facilitar a las personas designadas por el ICANE a tales efectos, la información y documentación que éstas soliciten para disponer de un pleno conocimiento de las circunstancias en que se desarrollan los trabajos, así como de los eventuales problemas que puedan plantearse y de las tecnologías,  métodos, y herramientas utilizados para resolverlos.

La documentación generada durante la ejecución del contrato de propiedad exclusiva del ICANE sin que el contratista pueda facilitarla a terceros sin la expresa autorización de este organismo, que la daría en su caso previa petición formal del contratista con expresión del fin.

Toda la documentación se entregará en los idiomas español o inglés en el sistema que se determine conjuntamente con el equipo técnico del ICANE.

El adjudicatario deberá suministrar al ICANE las nuevas versiones de la documentación que se vayan produciendo. También se entregará, en su caso, los documentos sobre los que se ha basado el desarrollo en idéntico soporte a los anteriores.

El código fuente estará en todo momento a disposición del equipo técnico del ICANE en un servidor de control de versiones a designar consensuadamente con el adjudicatario, siguiendo un modelo de trabajo *master-development-feature branches*.

Ofertas
-------
###Estructura normalizada y contenido de las ofertas
Con independencia de que el licitador pueda adjuntar a su oferta cuanta información complementaria considere de interés, deberá estar obligatoriamente estructurada de la siguiente forma:

####Índice
####Características generales
Identificación de la oferta, alcance e importe económico, acatamiento con carácter general a las condiciones del pliego y datos de empresa.
####Descripción de la solución técnica
Se incorporará en una columna adicional en los anexos de requisitos de este pliego el resumen de los aspectos más significativos y relevantes de la solución ofertada, requisito por requisito.
####Organización y estimación de los trabajos
Se entregará una estimación de esfuerzo inicial para la ejecución de las historias de usuario y requisitos en puntos/historia, en una columna adicional en los anexos de requisitos de este pliego. Dicha estimación será utilizada por los licitadores para elaborar su oferta económica. Asimismo, se ajustará durante la ejecución del proyecto y servirá para planificar los distintos ciclos del desarrollo.
####Oferta económica:
El coste total del proyecto se estimará de la siguiente forma:

    CT = SUMA(Fi) * Vd * C + ME

en donde:

- CT es el coste total en €.
- Fi es el número de puntos de esfuerzo estimados por cada característica, historia o requisito (y *SUMA()* es un sumatorio).
- Vd es la velocidad de desarrollo del adjudicatario en horas / punto.
- C es el coste medio de la hora de trabajo del adjudicatario en € / hora.
- ME es el margen de incertidumbre.

####Definición del equipo de trabajo
El adjudicatario detallará la composición del equipo de trabajo, así como los roles asumidos por cada uno de los participantes.
####Ejecución del contrato
Se incluirá en este capítulo la descripción de las medidas dispuestas por el oferente para asegurar la calidad de los trabajos; metodologías, medios materiales, seguridad y confidencialidad, así como aquellas otras que se prevé aplicar para vigilar y garantizar el adecuado cumplimiento del contrato.
####Otros datos técnicos
Aspectos que no estando relacionados anteriormente hayan sido solicitados en el pliego.

Sistema de decisión para la adjudicación
----------------------------------------
El único criterio de adjudicación será el precio, entendiéndose que la oferta económicamente más ventajosa es la que incorpora el precio más bajo.

Penalidades y resolución del contrato
-------------------------------------
Las propias del *Real Decreto Legislativo 3/2011, de 14 de noviembre, por el que se aprueba el texto refundido de la Ley de Contratos del Sector Público.* Concretamente:

###Demora
**Art. 212.4:** Cuando el contratista, por causas imputables al mismo, hubiere incurrido en demora respecto al cumplimiento del plazo total, la Administración podrá optar indistintamente por la resolución del contrato o por la imposición de las penalidades diarias en la proporción de 0,20 euros por cada 1.000 euros del precio del contrato.

###Ejecución defectuosa o incumplimiento
**Art 212.7:** Cuando el contratista, por causas imputables al mismo, hubiere incumplido la ejecución parcial de las prestaciones definidas en el contrato, la Administración podrá optar, indistintamente, por su resolución o por la imposición de las penalidades que, para tales supuestos, se determinen en el pliego de cláusulas administrativas particulares.

La ejecución defectuosa del contrato dará lugar a la imposición de una penalidad calculada de la siguiente forma:

Por cada requisito o historia de usuario incumplido o efectuado de forma defectuosa, se impondrá una penalización correspondiente a la parte proporcional de los puntos estimados para dicho requisito o historia con respecto al número total de puntos estimados para el contrato.

    Penalización(€) = Puntos ejecución defectuosa * Precio del contrato (€) / Nº de puntos estimados totales

La suma de las penalidades derivadas de los conceptos anteriores **no podrá ser superior al 10 por 100 del presupuesto del contrato.**

Las penalidades se impondrán por acuerdo inmediatamente ejecutivo del órgano de contratación a propuesta del responsable del contrato y se harán efectivas por retención en el pago.

Documentación anexa
-------------------
- Documento `requisitos_contratista.xls`: libro XLS 2003 con hojas para los distintos requisitos (funcionales, de calidad, de integración, etc.) así como historias de usuario.
- Directorio "flowchart": página web con diagramas de flujo y de estados del sistema.
- Directorio "mocks": página web con mocks de la interfaz del sistema.
- Documento `ficha_diseño.xls`: libro XLS 2003 con un ejemplo de ficha de diseño de cubos OLAP y notas con buenas prácticas.

Bibliografía
------------
* [BECK00]:"Extreme Programming Explained", Kent Beck.
* [COD00]: ["Código de buenas prácticas en las estadísticas europeas".](http://www.icane.es/icane/good-practices)
* [BELL00]: "Lean IT: Enabling and Sustaining Your Lean Transformation", Steven C. Bell, Michael A. Orzen.
* [BOB00]: "Agile Software Development, Principles, Patterns and Practices", Robert C. Martin.
* [FOWLER00]: "UML Distilled: A Brief Guide to the Standard Object Modeling Language", Martin Fowler.
* [FOWLER01]: "Refactoring: Improving the Design of Existing Code", Martin Fowler.
