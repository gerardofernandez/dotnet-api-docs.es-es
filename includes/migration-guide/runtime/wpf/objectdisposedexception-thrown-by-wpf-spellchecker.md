### <a name="objectdisposedexception-thrown-by-wpf-spellchecker"></a>ObjectDisposedException producida por el corrector ortográfico WPF

|   |   |
|---|---|
|Detalles|En ocasiones, las aplicaciones de WPF se bloquean durante el cierre de la aplicación con una <xref:System.ObjectDisposedException?displayProperty=name> producida por el corrector ortográfico. Esto se corrigió en .NET 4.7 WPF controlando la excepción correctamente y, lo que garantiza que las aplicaciones negativamente ya no se ven afectadas. Debe tenerse en cuenta que las excepciones de primera oportunidad ocasionales continuaría tenerse en cuenta en aplicaciones que se ejecutan bajo un depurador.|
|Sugerencia|Actualización a .NET 4.7|
|Ámbito|Borde|
|Versión|4.6.1|
|Tipo|Tiempo de ejecución|

