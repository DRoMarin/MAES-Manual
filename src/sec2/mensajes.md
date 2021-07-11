# Mensajes

Los mensajes transportan la información entre agentes; son etiquetados con 

+ Tipo de mensaje
+ Destinarario
+ Remitente 

EL usuario directamente no debe crear cada mensaje pues están contenidos dentro de los comportamientos de cada agente. Cada agente posee un buzón (cola de FreeRTOS) con longitud unitaria. Para administrar la información de los mensajes el usuario debe usar los métodos de la clase `Agent_Message`.


