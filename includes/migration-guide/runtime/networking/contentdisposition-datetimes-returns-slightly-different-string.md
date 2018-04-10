### <a name="contentdisposition-datetimes-returns-slightly-different-string"></a>ContentDisposition DateTimes devuelve la cadena ligeramente diferente

|   |   |
|---|---|
|Detalles|Representaciones de cadena de <xref:System.Net.Mime.ContentDisposition?displayProperty=name>de se han actualizado, a partir de la versión 4.6, que siempre representan el componente horario de un <xref:System.DateTime?displayProperty=name> con dos dígitos. La finalidad es cumplir con [RFC822](http://www.ietf.org/rfc/rfc0822.txt) y [RFC2822](http://www.ietf.org/rfc/rfc2822.txt). De este modo, <xref:System.Net.Mime.ContentDisposition.ToString> devuelve una cadena ligeramente diferente en escenarios de la versión 4.6 en los que uno de los elementos de hora de la disposición era anterior a las 10:00. Tenga en cuenta que ContentDispositions a veces se serializan a través de convertirlas en cadenas, por lo que cualquier <xref:System.Net.Mime.ContentDisposition.ToString> operaciones, serialización o GetHashCode llamadas deben revisarse.|
|Sugerencia|No espere que las representaciones de cadena de elementos ContentDisposition de otras versiones de .NET Framework se comparen correctamente entre sí. Vuelva a convertir las cadenas a elementos ContentDisposition, si fuera posible, antes de realizar una comparación.|
|Ámbito|Secundaria|
|Versión|4.6|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Net.Mime.ContentDisposition.ToString?displayProperty=nameWithType></li><li><xref:System.Net.Mime.ContentDisposition.GetHashCode?displayProperty=nameWithType></li></ul>|

