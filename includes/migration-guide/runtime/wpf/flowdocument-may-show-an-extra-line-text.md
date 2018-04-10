### <a name="flowdocument-may-show-an-extra-line-of-text"></a>FlowDocument puede mostrar una línea de texto adicional

|   |   |
|---|---|
|Detalles|En algunos casos, un <xref:System.Windows.Documents.FlowDocument> elemento mostrará una línea de texto adicional cuando se ejecuta en .NET Framework 4.5 en comparación a cómo se mostraba cuando se ejecuta en .NET Framework 4.0. No hay casos conocidos del cambio que se produce cualquier texto que se mostrará un rendimiento bajo o illegibly, pero podría provocar que aparezca el texto que anteriormente estaba omitido en un <xref:System.Windows.Documents.FlowDocument>de la vista.|
|Sugerencia|En algunos casos, reduciendo la presentación propiedad del elemento PageHeight en uno puede restaurar el número anterior de las líneas mostradas.|
|Ámbito|Borde|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Windows.Documents.FlowDocument.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Documents.FlowDocument.%23ctor(System.Windows.Documents.Block)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentReader.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentPageViewer.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.DocumentPageView.%23ctor?displayProperty=nameWithType></li></ul>|

