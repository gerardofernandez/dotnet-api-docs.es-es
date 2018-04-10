### <a name="unicode-standard-version-80-categories-now-supported"></a>Ahora se admiten las categorías Unicode estándar versión 8.0

|   |   |
|---|---|
|Detalles|En .NET Framework 4.6.2, datos Unicode en el marco de trabajo se ha actualizado de Unicode estándar versión 6.3 a la versión 8.0.  Cuando se solicita la categoría de caracteres Unicode en .NET Framework 4.6.2, algunos de los resultados podrían no coincidir los resultados en las versiones anteriores de .NET Framework.  Este cambio principalmente afecta a Cherokee sílabas y signos de las vocales Tai lue moderno nueva y marcas de tono.|
|Sugerencia|Revise el código y quitar o cambiar la lógica que dependa de las categorías de caracteres Unicode codificados de forma rígida.|
|Ámbito|Secundaria|
|Versión|4.6.2|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Char.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.String,System.Int32)?displayProperty=nameWithType></li></ul>|

