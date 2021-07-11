# Plataforma

La clase `Agent_Platform` administra el registro e inicialización de los agentes, así como métodos misceláneos para el controla de tareas. Los métodos de la clase son todos públicos aunque están condicionados al agente (o mejor dicho tarea) que les convoque. Los métodos se pueden visualizar como

+ Funciones pre-calendarizador
+ Funciones del Agente AMS
+ Funciones no restringidas. 

Las funciones pre-calendarizador inician los agentes y arrancan el registro de los objetos a las variables de entorno de la plataforma, para estas funcionar es necesario que ninguna tarea se esté ejecutando. Las funciones del Agente AMS corresponden a:

* Registros
* Dadas de baja
* Terminaciones
* Suspensión
* Reanudación de los agentes

Finalmente, las funciones no restringidas producen demoras en las tareas (_Task Delays_), buscan agentes, descripciones y estados de agentes; entre otros.

El constructor de esta clas solo solicita un parámetro; el nombre para la plataforma, sin embargo, puede iniciarse además con un parámetro más que defina las condiciones del Agente AMS mediante la clase `USER_DEF_COND`
