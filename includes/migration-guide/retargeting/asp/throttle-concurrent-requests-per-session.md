### <a name="throttle-concurrent-requests-per-session"></a>Límite de solicitudes simultáneas por sesión

|   |   |
|---|---|
|Detalles|En .NET Framework 4.6.2 y versiones anteriores, ASP.NET ejecuta las solicitudes con el mismo valor de Sessionid secuencialmente y ASP.NET siempre emite el valor de Sessionid a través de las cookies de forma predeterminada. Si una página tarda mucho tiempo en responder, reducirán considerablemente el rendimiento del servidor simplemente presionando F5 en el explorador. En la solución, hemos agregado un contador para realizar el seguimiento de las solicitudes en cola y las solicitudes de finalización cuando supera un límite especificado. El valor predeterminado es 50. Si se alcanza el límite, se registrará una advertencia en caso de registro y una respuesta HTTP 500 se pueden grabar en el registro de IIS.|
|Sugerencia|Para restaurar el comportamiento anterior, puede agregar la siguiente configuración al archivo web.config para rechazar el nuevo comportamiento.<pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;aspnet:RequestQueueLimitPerSession&quot; value=&quot;2147483647&quot;/&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;</code></pre>|
|Ámbito|Borde|
|Versión|4.7|
|Tipo|Redestinación|

