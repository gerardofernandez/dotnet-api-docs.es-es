### <a name="incorrect-implementation-of-memberdescriptorequals"></a>Implementación incorrecta de MemberDescriptor.Equals

|   |   |
|---|---|
|Detalles|La implementación original de &quot;es igual a&quot; método estaba comparando dos propiedades de cadena diferentes de los objetos situados debajo de comparación: nombre de la categoría a la cadena de descripción. La solución consiste en comparar &quot;categoría&quot; del primer objeto que &quot;categoría&quot; de la segunda y &quot;descripción&quot; a &quot;descripción&quot;. Valor de configuración de MemberDescriptorEqualsReturnsFalseIfEquivalent puede establecerse en true para descartar el nuevo comportamiento si el destino es 4.6.2 o en false para habilitar esta corrección cuando destinado a la versión de framework está por debajo de 4.6.2.|
|Sugerencia|Si la aplicación depende de MemberDescriptor.Equals a veces devuelve false cuando descriptores son equivalentes y su destino 4.6.2 versión de .NET Framework, tiene varias opciones:<ol><li>Realizar cambios de código para comparar &quot;categoría&quot; y &quot;descripción&quot; campos manualmente además de ejecutar el método Equals.</li><li>Dejar de participar en este cambio sumando el valor siguiente al archivo app.config:</li></ol><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Si los destinos de aplicación 4.6.1 o una versión anterior de .NET Framework y desea que este cambio habilitado, puede establecer el modificador de compatibilidad en false sumando el valor siguiente al archivo app.config:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Ámbito|Borde|
|Versión|4.6.2|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.ComponentModel.MemberDescriptor.Equals(System.Object)?displayProperty=nameWithType></li></ul>|

