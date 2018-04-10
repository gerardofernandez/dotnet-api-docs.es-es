### <a name="servicebase-doesnt-propagate-onstart-exceptions"></a>ServiceBase no propaga las excepciones de OnStart

|   |   |
|---|---|
|Detalles|4.7 de .NET Framework y versiones anteriores, las excepciones producidas en el inicio del servicio no se propagan al llamador del <xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType>. A partir de las aplicaciones que tienen como destino .NET Framework 4.7.1, el tiempo de ejecución propaga las excepciones a <xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType> para los servicios que no se inicie.|
|Sugerencia|Durante el inicio del servicio, si hay una excepción, esa excepción se propagará. Esto debería ayudar a diagnosticar casos donde podrá iniciar los servicios. Si no desea este comportamiento, pueden excluirse agregando las siguientes <AppContextSwitchOverrides> elemento a la <runtime> sección de su archivo de configuración de aplicación:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=true&quot; /&gt;&#13;&#10;</code></pre>Si la aplicación tiene como destino una versión anterior a 4.7.1 pero desea que este comportamiento, agregue el siguiente <AppContextSwitchOverrides> elemento a la <runtime> sección de su archivo de configuración de aplicación:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=false&quot; /&gt;&#13;&#10;</code></pre>|
|Ámbito|Secundaria|
|Versión|4.7.1|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase)?displayProperty=nameWithType></li><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase[])?displayProperty=nameWithType></li></ul>|

