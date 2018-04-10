### <a name="systemuriiswellformeduristring-method-returns-false-for-relative-uris-with-a-colon-char-in-first-segment"></a>Método System.Uri.IsWellFormedUriString devuelve false para identificadores URI relativos con un carácter de dos puntos en el primer segmento

|   |   |
|---|---|
|Detalles|A partir de .NET Framework 4.5, <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)> tratará identificadores URI relativos con una <code>:</code> en su primer segmento como no está bien formado. Se trata de un cambio con respecto a <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> comportamiento en .NET Framework 4.0 que se realizó para que se ajuste a RFC3986.|
|Sugerencia|Este cambio (por ejemplo, muchos otros cambios URI) solo afectará a las aplicaciones dirigidas a .NET Framework 4.5 (o posterior). Para seguir usando el comportamiento anterior, el destino de la aplicación en .NET Framework 4.0. Como alternativa, análisis del URI antes de llamar a <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> buscando <code>:</code> caracteres que se pueden quitar con fines de validación, si el comportamiento anterior es deseable.|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=nameWithType></li></ul>|

