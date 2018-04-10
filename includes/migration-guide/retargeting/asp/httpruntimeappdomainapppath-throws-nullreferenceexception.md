### <a name="httpruntimeappdomainapppath-throws-a-nullreferenceexception"></a>HttpRuntime.AppDomainAppPath lanza una excepción NullReferenceException

|   |   |
|---|---|
|Detalles|En .NET Framework 4.6.2, el runtime produce una <code>T:System.NullReferenceException</code> al recuperar un <code>P:System.Web.HttpRuntime.AppDomainAppPath</code> valor que incluye caracteres nulos. En .NET Framework 4.6.1 y versiones anteriores, el runtime produce una <code>T:System.ArgumentNullException</code>.|
|Sugerencia|Puede realizar una de las siguientes para responder a este cambio:<ul><li>Controlar la <code>T:System.NullReferenceException</code> si, su aplicación se ejecuta en .NET Framework 4.6.2.</li><li>Actualice a la 4.7 de Framework. NET, que restaura el comportamiento anterior y se produce un <code>T:System.ArgumentNullException</code>.</li></ul>|
|Ámbito|Borde|
|Versión|4.6.2|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.Web.HttpRuntime.AppDomainAppPath?displayProperty=nameWithType></li></ul>|

