### <a name="opt-in-break-to-revert-from-different-45-sql-generation-to-simpler-40-sql-generation"></a>Participación en salto para revertir desde diferentes 4.5 generación de SQL a la generación de SQL 4.0 más sencillo

|   |   |
|---|---|
|Detalles|Las consultas que producen instrucciones JOIN y contienen una llamada a una operación de limitación sin primero con OrderBy ahora producen un código SQL más sencillo. Después de actualizar a .NET Framework 4.5, estas consultas producían código SQL más complicado que en versiones anteriores.|
|Sugerencia|Esta característica está deshabilitada de manera predeterminada. Si Entity Framework genera instrucciones de combinación adicionales que causan una degradación del rendimiento, puede habilitar esta característica mediante la adición de la entrada siguiente en la <code>&lt;appSettings&gt;</code> sección del archivo de configuración (app.config) de aplicación:<pre><code class="language-xml">&lt;add key=&quot;EntityFramework_SimplifyLimitOperations&quot; value=&quot;true&quot; /&gt;&#13;&#10;</code></pre>|
|Ámbito|Transparente|
|Versión|4.5.2|
|Tipo|Tiempo de ejecución|

