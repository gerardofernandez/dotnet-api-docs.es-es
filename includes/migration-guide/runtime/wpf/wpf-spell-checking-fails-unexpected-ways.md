### <a name="wpf-spell-checking-fails-in-unexpected-ways"></a>Ortográfica de WPF se produce un error de forma inesperada

|   |   |
|---|---|
|Detalles|Esto incluye una serie de problemas de WPF corrector ortográfico:<ul><li>A veces produce WPF corrector ortográfico <xref:System.Runtime.InteropServices.COMException?displayProperty=name></li><li>Se produce un error en el corrector ortográfico de WPF con <xref:System.UnauthorizedAccessException> cuando las aplicaciones se inician con la opción 'Ejecutar como usuario diferente'</li><li>WPF corrector ortográfico identifica incorrectamente los errores de ortografía en palabras compuestas como 'Hausnummer' en alemán.</li></ul>|
|Sugerencia|Problema #1: Esto se ha solucionado en .NET Framework 4.6.2 problema 2 - ortográfica de WPF ya no se admite cuando las aplicaciones se inician con la opción 'Ejecutar como usuario diferente'. A partir de .NET Framework 4.6.2, iniciadas de esta manera las aplicaciones ya no se bloquearán inesperadamente, el corrector ortográfico en su lugar, se deshabilitará en modo silencioso. Problema #3: Esto se ha solucionado en .NET Framework 4.6.2.|
|Ámbito|Borde|
|Versión|4.6.1|
|Tipo|Tiempo de ejecución|

