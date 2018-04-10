### <a name="webutilityhtmlencode-and-webutilityhtmldecode-round-trip-bmp-correctly"></a>WebUtility.HtmlEncode y BMP de ida y vuelta de WebUtility.HtmlDecode correctamente

|   |   |
|---|---|
|Detalles|Para las aplicaciones que tienen como destino .NET Framework 4.5, caracteres que no pertenecen a la ida y vuelta de Basic Multilingual Plane (BMP) correctamente cuando se pasan a la <xref:System.Net.WebUtility.HtmlDecode(System.String)> métodos.|
|Sugerencia|Este cambio debe no tener ningún efecto en las aplicaciones actuales, pero para restaurar el comportamiento original, establezca la <code>targetFramework</code> atributo de la <code>&lt;httpRuntime&gt;</code> elemento a una cadena distinto &quot;4.5&quot;. También puede establecer los atributos <code>unicodeEncodingConformance</code> y <code>unicodeDecodingConformance</code> del elemento de configuración <code>&lt;webUtility&gt;</code> para controlar este comportamiento con independencia de la versión de .NET Framework que se use como destino.|
|Ámbito|Borde|
|Versión|4.5|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.Net.WebUtility.HtmlEncode(System.String)?displayProperty=nameWithType></li><li><xref:System.Net.WebUtility.HtmlEncode(System.String,System.IO.TextWriter)?displayProperty=nameWithType></li></ul>|

