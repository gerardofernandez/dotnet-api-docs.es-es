### <a name="winrt-stream-adapters-no-long-call-flushasync-automatically-on-close"></a>Adaptadores de flujo de WinRT no llamar a FlushAsync automáticamente al cerrar

|   |   |
|---|---|
|Detalles|En aplicaciones de la tienda de Windows, los adaptadores de secuencia en tiempo de ejecución de Windows ya no llaman al método de FlushAsync desde el método Dispose.|
|Sugerencia|Este cambio debe ser transparente. Los desarrolladores pueden restaurar el comportamiento anterior escribiendo código similar al siguiente:<pre><code class="language-csharp">using (var stream = GetWindowsRuntimeStream() as Stream)&#13;&#10;{&#13;&#10;// do something&#13;&#10;await stream.FlushAsync();&#13;&#10;}&#13;&#10;</code></pre>|
|Ámbito|Transparente|
|Versión|4.5.1|
|Tipo|Tiempo de ejecución|

