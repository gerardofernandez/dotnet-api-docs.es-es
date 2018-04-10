### <a name="wcf-msmqsecurehashalgorithm-default-value-is-now-sha256"></a>Valor predeterminado de WCF MsmqSecureHashAlgorithm ahora es SHA256

|   |   |
|---|---|
|Detalles|A partir de .NET Framework 4.7.1, el mensaje predeterminado que se firma el algoritmo de WCF para los mensajes de Msmq es SHA256. 4.7 de .NET Framework y versiones anteriores, el mensaje predeterminado de algoritmo de firma es SHA1.|
|Sugerencia|Si experimenta problemas de compatibilidad con este cambio en .NET Framework 4.7.1 o una versión posterior, se puede dejar el cambio agregando la siguiente línea a la <code>&lt;runtime&gt;</code>sección del archivo app.config:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InMsmqEncryptionAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Ámbito|Secundaria|
|Versión|4.7.1|
|Tipo|Tiempo de ejecución|

