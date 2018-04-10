### <a name="ef-no-longer-throws-for-queryviews-with-specific-characteristics"></a>EF ya no se produce para QueryViews con características específicas

|   |   |
|---|---|
|Detalles|Entity Framework ya no se produce un <xref:System.StackOverflowException?displayProperty=name> excepción cuando una aplicación ejecuta una consulta que usa QueryView con una de 0.. 1 propiedad de navegación que intenta incluir las entidades relacionadas como parte de la consulta. Por ejemplo, mediante una llamada a <code>.Include(e =&gt; e.RelatedNavProp)</code>.|
|Sugerencia|Este cambio solo afecta a código que usa QueryViews con 1-0 a 1 relaciones al que llaman las consultas se ejecutan. Incluir. Mejora la fiabilidad y debe ser transparente para casi todas las aplicaciones. Pero puede deshabilitarlo si causa un comportamiento inesperado; para ello, agregue la entrada siguiente a la sección <code>&lt;appSettings&gt;</code> del archivo de configuración de la aplicación:<pre><code class="language-xml">&lt;add key=&quot;EntityFramework_SimplifyUserSpecifiedViews&quot; value=&quot;false&quot; /&gt;&#13;&#10;</code></pre>|
|Ámbito|Borde|
|Versión|4.5.2|
|Tipo|Tiempo de ejecución|

