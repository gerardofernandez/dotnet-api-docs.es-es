### <a name="webutilityhtmldecode-no-longer-decodes-invalid-input-sequences"></a>WebUtility.HtmlDecode ya no se descodifica las secuencias de entrada no válidas

|   |   |
|---|---|
|Detalles|De forma predeterminada, los métodos de descodificación ya no descodifican secuencias de entrada no válidas en una cadena UTF-16 no válida. En su lugar, devuelven la entrada original.|
|Sugerencia|El cambio en la salida del descodificador solo es importante si se almacenan datos binarios en lugar de datos UTF-16 en cadenas. Para controlar explícitamente este comportamiento, establezca la <code>aspnet:AllowRelaxedUnicodeDecoding</code> atributo de la [appSettings](~/docs/framework/configure-apps/file-schema/appsettings/index.md) elemento <code>true</code> para activar el comportamiento heredado o a <code>false</code> para habilitar el comportamiento actual.|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Net.WebUtility.HtmlDecode(System.String)?displayProperty=nameWithType></li><li><xref:System.Net.WebUtility.HtmlDecode(System.String,System.IO.TextWriter)?displayProperty=nameWithType></li><li><xref:System.Net.WebUtility.UrlDecode(System.String)?displayProperty=nameWithType></li></ul>|

