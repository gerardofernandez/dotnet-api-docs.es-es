### <a name="enumerableemptylttresultgt-always-returns-cached-instance"></a>Enumerable.Empty&lt;TResult&gt; siempre devuelve en la caché de instancia

|   |   |
|---|---|
|Detalles|A partir de .NET 4.5, <xref:System.Linq.Enumerable.Empty%60%601> siempre devuelve una instancia interna almacenada en caché <xref:System.Collections.Generic.IEnumerable%601>. Anteriormente, <xref:System.Linq.Enumerable.Empty%60%601> podría almacenar en memoria caché vacío <xref:System.Collections.Generic.IEnumerable%601> en el momento en que se llamó a la API, lo que significa que en algunas condiciones en la que <xref:System.Linq.Enumerable.Empty%60%601> se llamó rápidamente y de forma simultánea, diferentes instancias del tipo se ha pudieron devolver para las distintas llamadas a la API.|
|Sugerencia|Puesto que el comportamiento anterior no era determinista, es poco probable que el código dependa de él. No obstante, en el improbable caso de que se comparen enumerables vacíos y que se espere que a veces sean distintos, deberían crearse matrices vacías explícitas (<code>new T[0]</code>) en lugar de usar <xref:System.Linq.Enumerable.Empty%60%601>.|
|Ámbito|Borde|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Linq.Enumerable.Empty%60%601?displayProperty=nameWithType></li></ul>|

