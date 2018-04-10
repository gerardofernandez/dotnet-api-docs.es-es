### <a name="wcf-message-security-now-is-able-to-use-tls11-and-tls12"></a>Seguridad de mensaje WCF ahora es capaz de usar TLS1.1 y TLS1.2

|   |   |
|---|---|
|Detalles|A partir de la 4.7 de .NET Framework, los clientes pueden configurar TLS1.1 o TLS 1.2 en la seguridad de mensaje WCF además SSL3.0 y TLS1.0 a través de los valores de configuración de aplicación.|
|Sugerencia|En el 4.7 de Framework. NET, compatibilidad con TLS1.1 y TLS1.2 en seguridad de mensaje WCF está deshabilitada de forma predeterminada. Puede habilitar agregando la siguiente línea a la <code>&lt;runtime&gt;</code> sección del archivo app.config o web.config:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableUsingServicePointManagerSecurityProtocols=false;Switch.System.Net.DontEnableSchUseStrongCrypto=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Ámbito|Borde|
|Versión|4.7|
|Tipo|Redestinación|

