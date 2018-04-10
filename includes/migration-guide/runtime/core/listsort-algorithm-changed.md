### <a name="listsort-algorithm-changed"></a>Algoritmo de List.Sort cambiado

|   |   |
|---|---|
|Detalles|A partir de .NET Framework 4.5, <xref:System.Collections.Generic.List%601?displayProperty=name>del algoritmo de ordenación ha cambiado (para que sea una ordenación introspectivas en lugar de una ordenación rápida). <xref:System.Collections.Generic.List%601?displayProperty=name>de ordenación nunca ha sido estable, pero este cambio puede provocar distintos escenarios ordenar de maneras inestable. Esto simplemente significa que pueden ordenar los elementos equivalentes en distintas órdenes en las llamadas subsiguientes de la API.|
|Sugerencia|Dado que el algoritmo de ordenación anterior también estaba inestable (aunque de forma ligeramente diferente), no debería haber ningún código que depende de los elementos equivalentes siempre ordenar en un orden concreto. Si hay instancias de función de el código y está de suerte con el comportamiento anterior, que el código debe actualizarse para utilizar a un comparador que se ordenará de forma determinista los elementos en el orden deseado.|
|Ámbito|Transparente|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Collections.Generic.List%601.Sort?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Comparison{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Int32,System.Int32,System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li></ul>|

