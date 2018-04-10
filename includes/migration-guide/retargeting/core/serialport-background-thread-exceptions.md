### <a name="serialport-background-thread-exceptions"></a>Excepciones de subproceso de fondo SerialPort

|   |   |
|---|---|
|Detalles|Los subprocesos creados con en segundo plano <xref:System.IO.Ports.SerialPort> secuencias ya no finalizan el proceso cuando se produzcan excepciones de sistema operativo. En las aplicaciones destinadas a .NET Framework 4.7 y versiones anteriores, se termina un proceso cuando se produce una excepción de sistema operativo en un subproceso en segundo plano creado con una <xref:System.IO.Ports.SerialPort> secuencia. En aplicaciones que destino es .NET Framework 4.7.1 o una versión posterior, subprocesos en segundo plano esperan eventos del sistema operativo relacionados con el puerto serie activo y pudieron dejar de funcionar en algunos casos, como la eliminación repentina del puerto serie.|
|Sugerencia|Para las aplicaciones que tienen como destino .NET Framework 4.7.1, puede rechazar el control de excepciones si no es deseable debe agregar lo siguiente a la <code>&lt;runtime&gt;</code> sección de su <code>app.config</code> archivo:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Para las aplicaciones que tienen como destino versiones anteriores de .NET Framework pero se ejecutan en .NET Framework 4.7.1 o una versión posterior, puede participar en la excepción de control mediante la adición de las siguientes acciones para la <code>&lt;runtime&gt;</code> sección de su <code>app.config</code> archivo:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Ámbito|Secundaria|
|Versión|4.7.1|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.IO.Ports.SerialPort?displayProperty=nameWithType></li></ul>|

