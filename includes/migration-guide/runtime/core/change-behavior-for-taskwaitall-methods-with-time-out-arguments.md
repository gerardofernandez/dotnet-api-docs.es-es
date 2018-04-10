### <a name="change-in-behavior-for-taskwaitall-methods-with-time-out-arguments"></a>Cambio en el comportamiento para Task.WaitAll métodos con argumentos de tiempo de espera

|   |   |
|---|---|
|Detalles|Comportamiento de Task.WaitAll se realizó más coherente en .NET 4.5.In .NET Framework 4, estos métodos se comportaban de forma incoherente. Cuando se agotaba el tiempo de espera, si una o varias tareas se completaban o cancelaban antes de la llamada al método, el método producía una excepción <xref:System.AggregateException?displayProperty=name>. Cuando se agotaba el tiempo de espera, si no se completaba ni cancelaba ninguna tarea antes de la llamada al método, pero una o varias tareas entraban en estos estados después de la llamada al método, el método pasaba a ser false.<br/><br/>En .NET Framework 4.5, estas sobrecargas de método ahora devuelven false si las tareas siguen en ejecución cuando se agotó el intervalo de tiempo de espera y producen una <xref:System.AggregateException?displayProperty=name> excepción solo si se ha cancelado una tarea de entrada (independientemente de si formaba antes o después del método llamar a) y ninguna otra tarea en ejecución.|
|Sugerencia|Si un <xref:System.AggregateException?displayProperty=name> que se detectó como un medio para detectar una tarea que se canceló antes de la llamada WaitAll que se invoca, que el código en su lugar, debe hacer la misma detección a través de la propiedad IsCanceled (por ejemplo:. Any(t =&gt; t.IsCanceled)) dado que .NET 4.6 sólo se producirá en ese caso si todas las tareas de esperadas son secundarios antes de que el tiempo de espera.|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32,System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.TimeSpan)?displayProperty=nameWithType></li></ul>|

