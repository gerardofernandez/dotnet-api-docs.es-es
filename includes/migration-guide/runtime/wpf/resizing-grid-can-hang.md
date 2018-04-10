### <a name="resizing-a-grid-can-hang"></a>Cambiar el tamaño de una cuadrícula puede dejar de responder

|   |   |
|---|---|
|Detalles|Un bucle infinito puede producirse durante el diseño de un <code>T:System.Windows.Controls.Grid</code> en las siguientes circunstancias:<ul><li>Las definiciones de filas contienen dos *-filas, ambos declarar un MinHeight y un MaxHeight.</li><li>Contenido de la *-filas no supera la MaxHeight correspondiente</li><li>Alto disponible de la cuadrícula es superado por el primer MinHeight (más cualquier otro rol fijo o automáticamente filas)</li><li>La aplicación tiene como destino .net 4.7 o participar en el algoritmo de 4,7 asignación estableciendo <code>Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=false</code></li></ul>El bucle también podría ocurrir con más de dos filas, o en el caso similar para las columnas. El problema se corregirá en .net 4.7.1.|
|Sugerencia|Actualización a .net 4.7.1.  O bien, si ya no necesita el algoritmo de 4,7 asignación puede usar la opción de configuración siguiente:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Ámbito|Borde|
|Versión|4.7|
|Tipo|Tiempo de ejecución|

