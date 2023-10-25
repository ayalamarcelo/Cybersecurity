# Principios de seguridad

En el entorno laboral, los principios de seguridad están integrados en las tareas diarias. Ya sea que estés analizando registros, monitoreando un panel de gestión de eventos e información de seguridad (SIEM) o usando un escáner de vulnerabilidades,  utilizarás estos principios de alguna manera. 

Anteriormente, te presentamos varios principios de seguridad de OWASP, que incluían:

    Minimizar la superficie expuesta a ataques: se refiere a todas las vulnerabilidades potenciales que podría aprovechar un agente de amenaza.

    Principio de mínimo privilegio: significa conceder únicamente el acceso y la autorización mínimos necesarios para completar una tarea o función.

    Defensa en profundidad: hace referencia a que las organizaciones deben disponer de varios controles de seguridad que aborden los riesgos y las amenazas de diferentes maneras.

    Separación de funciones: refiere a que las acciones críticas deben depender de varias personas, cada una de las cuales sigue el principio del mínimo privilegio. 

    Simplificar la seguridad: tiene que ver con evitar soluciones innecesariamente complicadas, porque la complejidad dificulta la seguridad. 

    Solucionar los problemas de seguridad correctamente: significa que, cuando ocurren incidentes de seguridad, es necesario identificar la causa, contener el impacto, detectar las vulnerabilidades y realizar pruebas para garantizar que la reparación sea exitosa.

### Otros principios de seguridad de OWASP

A continuación, aprenderás acerca de otros cuatro principios de seguridad de OWASP que se utilizan para mantener seguras las operaciones de una organización y a las personas.
Establecer configuraciones seguras por defecto

Este principio indica que el estado de seguridad óptimo de una aplicación también debe ser su estado predeterminado para los/las usuarios/as. O sea, debería requerirse un esfuerzo adicional para hacer que la aplicación sea insegura. 
Fallar de forma segura

Fallar de forma segura significa que, cuando un control falla o se detiene, debe hacerlo restableciéndose automáticamente a su opción más segura. Por ejemplo, si un cortafuegos (firewall) falla, simplemente, debería cerrar todas las conexiones y bloquear las nuevas, en lugar de comenzar a aceptar todo.
No confiar en los servicios

Muchas organizaciones trabajan con firmas asociadas o proveedoras de servicios. Estas suelen tener políticas de seguridad diferentes a las de la empresa. Por lo tanto, la compañía no debería dar por sentado que los sistemas de estas firmas sean seguros. Por ejemplo, si una aerolínea terceriza a una empresa proveedora el seguimiento de los puntos de recompensa, antes de compartir esa información con sus clientes, debería asegurarse de que los datos obtenidos y el saldo sean precisos.
Evitar la seguridad por oscuridad

La seguridad de los sistemas clave no debe depender de mantener los detalles ocultos. Analiza el siguiente ejemplo de OWASP (2016):

La seguridad de una aplicación no debe depender de mantener el código fuente en secreto, sino que su seguridad tiene que basarse en muchos otros factores, como las políticas de contraseñas razonables, la defensa en profundidad, los límites de transacciones comerciales, una sólida arquitectura de red, y los controles de fraude y auditoría.

## Auditorías de seguridad

Existen dos tipos principales de auditorías de seguridad: externas e internas. Nos centraremos en las internas porque ese es el tipo de auditorías al que contribuyen los analistas de nivel inicial. La `auditoría interna` de seguridad la suele realizar un equipo de personas que puede incluir al encargado de cumplimiento, gerente de seguridad y otros miembros del equipo. Las auditorías internas de seguridad se utilizan para mejorar la postura de seguridad de una organización y evitar multas de agencias reguladoras por falta de cumplimiento normativo. Con la auditoría interna, el equipo identifica el riesgo organizacional, evalúa los controles y corrige problemas de cumplimiento. Ahora, que hemos discutido los propósitos de las auditorías internas, veamos algunos de sus componentes comunes. Estos son definir el alcance y los objetivos de la auditoría, evaluar el riesgo de los activos de la organización, evaluar el cumplimiento y comunicar los resultados a las partes interesadas. En este video, veremos los primeros dos elementos, que conforman el proceso de planificación: definir el alcance y los objetivos, y evaluar el riesgo. El alcance se refiere a los criterios de una auditoría interna. El alcance requiere identificar las personas, activos, políticas, procedimientos y tecnologías que podrían afectar a la postura de seguridad. Los objetivos son un planteo de las metas de seguirdad o qué se quiere lograr para mejorar la postura de seguridad. Aunque los miembros de mayor jerarquía del equipo de seguridad y otras partes interesadas suelen definir el alcance y los objetivos, a los analistas de nivel inicial se les puede pedir que revisen el alcance y los objetivos, a los analistas de nivel inicial se les puede pedir que revisen el alcance y los objetivos para completar otros elementos de la auditoría. A modo de ejemplo, el alcance de esta auditoría implica evaluar los permisos del usuario, identificar los controles, políticas y procedimieintos actuales y tener en cuenta latecnología utilizada actualmente por la organización. Los objetivos señalados incluyen implementar funciones centrales de los marcos, como el CSF del NIST, definir políticas y procedimientos para garantizar el cumplimiento normativo, y fortalecer los controles del sistema. El siguiente elemento es evaluar el riesgo, que se centra en identificar amenazas, riesgos, y vulnerabilidades potenciales. Esto ayuda a las organizaciones a decidir qué medidas de seguridad implementar y monitorear para proteger sus activos. Al igual que definir el alcance y los objetivos, suele evaluar el riesgo los gerentes u otras partes interesadas. Pero se te puede pedir que analices los detalles de la evaluación del riesgo para ver qué tipos de controles y normativa de cumplimientos se necesita tener para mejorar la postura de seguridad organizacional. Por ejemplo, esta evaluación del riesgo destaca que hay controles, procesos y procedimientos inadecuados para proteger los activos. En particular, falta un manejo adecuado de activos físicos y digitales, incluidos los equipos del personal. El equipo usado para almacenar datos no está bien protegido. Y el acceso a la información privada almacenada en la red interna necesita tener controles más sólidos. Tras ver los elementos iniciales de la planificación de una auditoría de seguridad interna.

### Realizar una auditoría

Antes vimos los elementos iniciales de una auditoría interna de seguridad.En este video, veremos los elementos finales que un/a analista de nivel inicial podría tener que completar. Recuerda: los elementos de planificación de las auditorías internas son definir el alcance y los objetivos, y evaluar los riesgos. Los elementos restantes son evaluar los controles,evaluar el cumplimiento y comunicar los resultados. Antes de completar los tres elementos finales debes consultar el alcance y los objetivos, así como la evaluación del riesgo, y plantearte algunas preguntas. Por ejemplo:
¿Qué se quiere lograr con la auditoría?
¿Qué activos están más en riesgo?
¿Son suficientes los controles actuales para proteger esos activos? Si no lo son, ¿qué controles y normativa de cumplimiento se deben implementar? Al tener en cuenta estas preguntas dispondrás de una base para completar el siguiente elemento: evaluar los controles. Una evaluación de controles implica revisar los activos de una organización y luego evaluar los posibles riesgos para esos activos a fin de garantizar que los controles internos sean efectivos.
Para lograrlo, los/las analistas de nivel inicial podrían clasificar los controles en las siguientes categorías. Controles administrativos, controles técnicos y controles físicos. Los controles administrativos se relacionan con el componente humano de la ciberseguridad. Son políticas y procedimientos que definen cómo una organización gestiona los datos,
como la implementación de las políticas de contraseñas. Los controles técnicos son soluciones de hardware y software para proteger los activos, como usar sistemas de detección de intrusiones (IDS) y cifrado. Los controles físicos son medidas implementadas para evitar el acceso físico a los activos protegidos, como cámaras de vigilancia y cerraduras. El siguiente elemento es determinar si la organización sigue o no el cumplimiento normativo necesaria. Recuerda, el cumplimiento normativo se refiere a leyes que la organización debe seguir para proteger los datos privados. En este ejemplo, la organización opera en la Unión Europea y acepta pagos con tarjeta de crédito. Por lo tanto, debe cumplir con el RGPD y los estándares de seguridad de datos del sector de las tarjetas de pago (PCI DSS). El elemento final de una auditoría interna de seguridad es la comunicación. Tras completar la auditoría interna, deben notificarse los resultados y recomendaciones a las partes interesadas. En general, este tipo de comunicación resume el alcance y los objetivos de la auditoría. Enumera los riesgos existentes e indica con qué velocidad deben abordarse. Además, identifica el cumplimiento normativo que la organización debe seguir y da recomendaciones para mejorar la postura de seguridad de la empresa. Las auditorías internas sirven para identificar vulnerabilidades dentro de la organización.

### Más información de las auditorías

* Auditorías de seguridad:

Una auditoría de seguridad es una revisión de los controles, políticas y procedimientos de seguridad de una organización. Las auditorías son revisiones independientes que evalúan si una compañía acata los criterios internos, como políticas, procedimientos y prácticas recomendadas, y externos, como el cumplimiento de normas, leyes y regulaciones federales.

Además, una auditoría de seguridad se puede utilizar para evaluar los controles de seguridad establecidos por una organización. Recuerda que los controles de seguridad son medidas diseñadas para reducir riesgos de seguridad específicos. 

Asimismo, las auditorías ayudan a garantizar que se realicen verificaciones de seguridad (por ejemplo, monitoreo diario de paneles de gestión de eventos e información de seguridad) para identificar amenazas, riesgos y vulnerabilidades. Esto ayuda a mantener la postura de seguridad de una organización. Y, si hay problemas de seguridad, se debe contar con un plan de acción correctiva.

### Metas y objetivos de una auditoría

La meta de una auditoría es garantizar que las prácticas de tecnología de la información (TI) de una organización cumplan con los estándares de la industria y de la propia organización. El objetivo es identificar y abordar las áreas que requieren mejoras y desarrollo. Las auditorías proporcionan dirección y claridad al identificar las fallas actuales y desarrollar un plan para corregirlas. 

Las auditorías de seguridad deben realizarse para proteger los datos y evitar sanciones y multas por parte de agencias gubernamentales. La frecuencia de las auditorías depende de las leyes locales y las regulaciones de cumplimiento normativo federal.
Factores que determinan las auditorías

Los factores que determinan los tipos de auditorías que una organización debe implementar incluyen: 

    Tipo de industria

    Tamaño de la organización

    Vínculos con las regulaciones gubernamentales 

    Ubicación geográfica de la empresa

    Decisión comercial de regirse por determinado cumplimiento normativo

Para revisar las regulaciones de cumplimiento normativo comunes a las que las diferentes organizaciones deben adherirse, consulta la lectura sobre controles, marcos y cumplimiento.

### El papel de los marcos y controles en las auditorías

Además del cumplimiento normativo, es importante mencionar el papel que desempeñan los marcos y controles en las auditorías de seguridad. Algunos marcos, como el Marco de Ciberseguridad (CSF) del Instituto Nacional de Estándares y Tecnología (NIST) y la serie de normas internacionales para la seguridad de la información (ISO 27000), están diseñados para ayudar a las organizaciones a prepararse para las auditorías de seguridad de cumplimiento normativo. Al adherirse a estos y otros marcos pertinentes, las empresas pueden ahorrar tiempo al realizar auditorías externas e internas. Además, cuando se utilizan junto con los controles, los marcos pueden respaldar la capacidad de las  organizaciones para cumplir con los requisitos y estándares de cumplimiento normativo.

### Lista de control de la auditoría

Antes de realizar una auditoría, es necesario crear una lista de control, que suele incluir los siguientes pasos:
Identifica el ámbito de la auditoría

    La auditoría debería:

        Enumerar los activos que se evaluarán, por ejemplo, si los cortafuegos (firewalls) están bien configurados, si la información personal de identificación (PII) es segura, si los activos físicos están bloqueados, etc.. 

        Especificar de qué manera la auditoría ayudará a la organización a alcanzar sus objetivos.

        Indicar la frecuencia con la que debería realizarse.

        Incluir una evaluación de las políticas, protocolos y procedimientos de la organización para asegurar que funcionen según lo previsto y que el personal los esté poniendo en práctica.

Completa una evaluación de riesgos

    Una evaluación de riesgos se utiliza para analizar los riesgos organizacionales identificados, relacionados con el presupuesto, los controles, los procesos internos y los estándares externos (por ejemplo, regulaciones).

Realiza una auditoría

    Al realizar una auditoría interna, evaluarás la seguridad de los activos identificados que se mencionan en el alcance de la auditoría.

Crea un plan de mitigación

    Un plan de mitigación es una estrategia implementada para reducir el nivel de riesgo y los costos potenciales, sanciones u otros problemas que puedan perjudicar la postura de seguridad de la organización. 

Comunica los resultados a las partes interesadas

    El resultado final de este proceso es proporcionar un informe detallado de los hallazgos, las mejoras sugeridas necesarias para reducir el nivel de riesgo de la organización, así como las normas y los estándares de cumplimiento que la empresa debe cumplir.

### Conclusiones clave

En esta lección, aprendiste más sobre las auditorías de seguridad, incluyendo su definición, el propósito de su realización y el papel que desempeñan los marcos, los controles y el cumplimiento normativo en dicho proceso. 

Si bien todavía queda mucho más por aprender sobre este tema, esta introducción tiene como objetivo brindarte apoyo para que puedas realizar una auditoría propia como parte de una actividad de autorreflexión en tu cartera, más adelante en este curso.