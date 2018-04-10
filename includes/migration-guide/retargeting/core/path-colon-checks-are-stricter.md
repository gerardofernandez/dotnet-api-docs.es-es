### <a name="path-colon-checks-are-stricter"></a>Comprobaciones de dos puntos de ruta de acceso son más estrictas

|   |   |
|---|---|
|Detalles|En .NET Framework 4.6.2, un número de cambios se realizaron para admitir las rutas de acceso anteriormente no admitidos (tanto en longitud y el formato). Comprobaciones de sintaxis de unidad correspondiente separador (dos puntos) se realizaron más correctas, que tenía el efecto secundario de bloqueo algunas rutas de acceso URI en donde usa para tolerar algunas API de ruta de acceso select.|
|Sugerencia|Si pasa un URI a las API afectadas, modifique la cadena para que sea una ruta de acceso válida en primer lugar.<ul><li>Quite manualmente el esquema de direcciones URL (por ejemplo, quitar <code>file://</code> de direcciones URL)</li><li>Pasar el URI para el <xref:System.Uri> clase y usar <xref:System.Uri.LocalPath></li></ul>Como alternativa, puede rechazar la normalización de la ruta de acceso nuevo estableciendo la <code>Switch.System.IO.UseLegacyPathHandling</code> conmutador AppContext en true.|
|Ámbito|Borde|
|Versión|4.6.2|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.IO.Path.GetDirectoryName(System.String)?displayProperty=nameWithType></li><li><xref:System.IO.Path.GetPathRoot(System.String)?displayProperty=nameWithType></li></ul>|

