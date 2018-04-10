### <a name="certificate-eku-oid-validation"></a>Validación de certificados EKU OID

|   |   |
|---|---|
|Detalles|A partir de .NET Framework 4.6, la <xref:System.Net.Security.SslStream> o <xref:System.Net.ServicePointManager> clases realizan la validación de identificador (OID) de objeto de uso mejorado de clave (EKU). Una extensión de uso mejorado de clave (EKU) es una colección de identificadores de objeto (OID) que indican las aplicaciones que usan la clave. Validación de EKU OID utiliza las devoluciones de llamada del certificado remoto para asegurarse de que el certificado remoto tiene los OID correctos para el propósito planteado.|
|Sugerencia|Si no deseado este cambio, puede deshabilitar EKU OID validación del certificado mediante la adición de cambie lo siguiente a la [ \<AppContextSwitchOverrides >](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) en el [ ` ](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) de su archivo de configuración de aplicación:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Net.DontCheckCertificateEKUs=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre> <blockquote> [!IMPORTANT] Esta configuración se proporciona por razones de compatibilidad. En caso contrario, no se recomienda su uso.</blockquote> |
|Ámbito|Secundaria|
|Versión|4.6|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.Net.Security.SslStream?displayProperty=nameWithType></li><li><xref:System.Net.ServicePointManager?displayProperty=nameWithType></li><li><xref:System.Net.Http.HttpClient?displayProperty=nameWithType></li><li><xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType></li><li><xref:System.Net.HttpWebRequest?displayProperty=nameWithType></li><li><xref:System.Net.FtpWebRequest?displayProperty=nameWithType></li></ul>|

