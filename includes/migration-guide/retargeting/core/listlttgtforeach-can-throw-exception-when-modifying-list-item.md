### <a name="listlttgtforeach-can-throw-exception-when-modifying-list-item"></a>Lista&lt;T&gt;. ForEach puede producir la excepción cuando se modifica el elemento de lista

|   |   |
|---|---|
|Detalles|A partir de .NET 4.5, un <xref:System.Collections.Generic.List%601.ForEach(System.Action{%600})> enumerador producirá un <xref:System.InvalidOperationException?displayProperty=name> excepción si se modifica un elemento de la colección que realiza la llamada. En versiones anteriores no se iniciaban excepciones en estos casos, aunque sí podían producirse condiciones de carrera.|
|Sugerencia|Lo ideal es corregir el código para no modificar listas durante la enumeración de sus elementos, ya que esta nunca es una operación segura. No obstante, para revertir al comportamiento anterior, es posible seleccionar .NET 4.0 como destino de una aplicación.|
|Ámbito|Borde|
|Versión|4.5|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.Collections.Generic.List%601.ForEach(System.Action{%600})?displayProperty=nameWithType></li></ul>|

