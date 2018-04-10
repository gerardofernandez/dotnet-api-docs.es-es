### <a name="wcf-pipeconnectiongethashalgorithm-now-uses-sha256"></a>WCF PipeConnection.GetHashAlgorithm ahora utiliza SHA256

|   |   |
|---|---|
|Detalles|A partir de .NET Framework 4.7.1, Windows Communication Foundation usa un algoritmo hash SHA256 para generar nombres aleatorios para canalizaciones con nombre. 4.7 de .NET Framework y versiones anteriores, usa un hash SHA1.|
|Sugerencia|Si experimenta el problema de compatibilidad con este cambio en .NET Framework 4.7.1 o una versión posterior, puede dejar agregando la siguiente línea a la <code>&lt;runtime&gt;</code> sección del archivo app.config:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InPipeConnectionGetHashAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Ámbito|Secundaria|
|Versión|4.7.1|
|Tipo|Tiempo de ejecución|

