### <a name="only-tls-10-11-and-12-protocols-supported-in-systemnetservicepointmanager-and-systemnetsecuritysslstream"></a>Sólo se admite en el objeto y System.Net.Security.SslStream protocolos de Tls 1.0, 1.1 y 1.2

|   |   |
|---|---|
|Detalles|A partir de la versión 4.6 de .NET Framework, el <xref:System.Net.ServicePointManager> y <xref:System.Net.Security.SslStream> sólo se permiten que las clases para utilizar uno de los siguientes tres protocolos: Tls1.0, Tls1.1 o TLS 1.2. No se admite el protocolo SSL 3.0 ni el cifrado RC4.|
|Sugerencia|La mitigación recomendada consiste en actualizar la aplicación del lado servidor a TLS 1.0, Tls1.1 o TLS 1.2. Si esto no es posible o si las aplicaciones cliente se interrumpen, se puede usar la clase <xref:System.AppContext?displayProperty=name> para descartar esta característica de cualquiera de estas dos maneras:<ol><li>Estableciendo mediante programación compat enciende el <xref:System.AppContext?displayProperty=name>, como se explicó [aquí](http://blogs.msdn.com/b/dotnet/archive/2015/04/29/net-announcements-at-build-2015.aspx#dotnet46)</li><li>Agregando la siguiente línea a la <code>&lt;runtime&gt;</code> sección del archivo app.config: <code>&lt;AppContextSwitchOverrides value=&quot;Switch.System.Net.DontEnableSchUseStrongCrypto=true&quot;/&gt;</code>;</li></ol>|
|Ámbito|Secundaria|
|Versión|4.6|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.Net.SecurityProtocolType.Ssl3?displayProperty=nameWithType></li><li><xref:System.Security.Authentication.SslProtocols.None?displayProperty=nameWithType></li><li><xref:System.Security.Authentication.SslProtocols.Ssl2?displayProperty=nameWithType></li><li><xref:System.Security.Authentication.SslProtocols.Ssl3?displayProperty=nameWithType></li></ul>|

