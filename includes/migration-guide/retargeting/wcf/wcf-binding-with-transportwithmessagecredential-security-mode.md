### <a name="wcf-binding-with-the-transportwithmessagecredential-security-mode"></a>Enlace de WCF con el modo de seguridad TransportWithMessageCredential

|   |   |
|---|---|
|Detalles|A partir de .NET Framework 4.6.1, enlace de WCF que utiliza el modo de seguridad TransportWithMessageCredential puede configurarse para recibir los mensajes sin firmar &quot;a&quot; encabezados para las claves de seguridad asimétrico. De forma predeterminada, no firmado &quot;a&quot; encabezados continuarán rechazarán en .NET 4.6.1. Sólo aceptarán si una aplicación opta por participar en este nuevo modo de operación mediante el modificador de configuración Switch.System.ServiceModel.AllowUnsignedToHeader. Dado que es una característica opcional, no debería afectar al comportamiento de las aplicaciones existentes.|
|Sugerencia|Como es una característica opcional, no debería afectar al comportamiento de las aplicaciones existentes. Para controlar si se utiliza el nuevo comportamiento o no, utilice la opción de configuración siguiente:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.AllowUnsignedToHeader=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Ámbito|Transparente|
|Versión|4.6.1|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.ServiceModel.BasicHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.BasicHttpsSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.WSFederationHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li></ul>|

