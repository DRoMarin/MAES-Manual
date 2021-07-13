# Derivación y Encapsulado de comportamientos

A partir de las clases `Generic_Behaviour`,` OneShotBehaviour` y `CyclicBehaviour` se deben describir la función de tarea como una subclase derivada. El método `setup()` define ajustes previos a un lazo de ejecución, el método `action()` describe la función principal de la tarea, los métodos `failure_detection()`, `failure_identification()` y `failure_recovery()` corresponden a los métodos para detección, identificación y recuperación de fallas respectivamente, y por último el método done() revisa si la función principal debe o no volver a ejecutarse.  El orden de ejecución está coordinado por el método `execute()` cuyo diagrama se describe en la sección 2. Dentro de este flujo se debe definir a que agente se envían que mensajes y cuando esperar por mensajes (mediante la variable msg y los métodos de la clase `Agent_Msg`). Para ser incluidos en la tarea, el método `execute()` de cada subclase definida debe contenerse dentro de una función encapsuladora con el siguiente formato (incluyendo el caso de usar parámetros):

```c++
void  FuncionEncap(void* parametros)
{
ComportamientoAgente b;
b.taskParameters = parametros;
b.execute();
}
```

