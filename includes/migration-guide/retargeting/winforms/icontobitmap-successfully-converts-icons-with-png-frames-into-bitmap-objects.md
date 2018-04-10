### <a name="icontobitmap-successfully-converts-icons-with-png-frames-into-bitmap-objects"></a>Icon.ToBitmap convierte correctamente iconos con marcos PNG en objetos de mapa de bits

|   |   |
|---|---|
|Detalles|A partir de las aplicaciones que tienen como destino la versión 4.6 de .NET Framework, el <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> método convierte correctamente iconos con marcos PNG en objetos de mapa de bits. En aplicaciones que tienen como destino .NET Framework 4.5.2 y versiones anteriores, el <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> método produce una <xref:System.ArgumentOutOfRangeException> excepción si el objeto de icono tiene marcos PNG. Este cambio afecta a las aplicaciones que se vuelven a compilar para tener como destino .NET Framework 4.6 y que implementan un tratamiento especial para el <xref:System.ArgumentOutOfRangeException> que se produce cuando un objeto Icon tiene marcos PNG. Cuando se ejecuta en .NET Framework 4.6, la conversión es correcta, ya no se genera un <xref:System.ArgumentOutOfRangeException> y, por tanto, ya no se invoca el controlador de excepciones.|
|Sugerencia|Si no desea este comportamiento, puede conservar el comportamiento anterior agregando el siguiente elemento en la <code>&lt;runtime&gt;</code> sección del archivo app.config:<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true&quot; /&gt;&#13;&#10;</code></pre>Si el archivo app.config ya contiene el <code>AppContextSwitchOverrides</code> elemento, el nuevo valor se debe combinar con el atributo de valor similar al siguiente:<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true;&lt;previous key&gt;=&lt;previous value&gt;&quot; /&gt;&#13;&#10;</code></pre>|
|Ámbito|Secundaria|
|Versión|4.6|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.Drawing.Icon.ToBitmap?displayProperty=nameWithType></li></ul>|

