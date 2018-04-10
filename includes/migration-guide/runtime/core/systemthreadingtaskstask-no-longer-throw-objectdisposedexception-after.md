### <a name="systemthreadingtaskstask-no-longer-throw-objectdisposedexception-after-object-is-disposed"></a>System.Threading.Tasks.Task ya no producen ObjectDisposedException después se elimina el objeto

|   |   |
|---|---|
|Detalles|Excepto para <xref:System.Threading.Tasks.Task.System%23IAsyncResult%23AsyncWaitHandle>, <xref:System.Threading.Tasks.Task?displayProperty=name> métodos ya no producen un <xref:System.ObjectDisposedException?displayProperty=name> excepción después de desechar el objeto. Este cambio admite el uso de tareas almacenados en caché. Por ejemplo, un método puede devolver una tarea almacenada en caché para representar una operación completada en lugar de asignar una nueva tarea. Esto no era posible en versiones anteriores de .NET Framework, ya que cualquier consumidor de la tarea podía desecharla, lo que hacía que se volviera inutilizable.|
|Sugerencia|Tenga en cuenta que ya no se pueden producir métodos tareas <xref:System.ObjectDisposedException?displayProperty=name> en casos cuando se elimina el objeto. Si una aplicación se dependiendo de que sabe que una tarea se ha cancelado esta excepción, se debe actualizar para comprobar el estado de la tarea de forma explícita mediante <xref:System.Threading.Tasks.Task.Status>.|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Tiempo de ejecución|

