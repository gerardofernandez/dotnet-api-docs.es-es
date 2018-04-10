### <a name="xmlschemaexception-now-sets-line-positions-properly"></a>XmlSchemaException ahora establece las posiciones de línea correctamente

|   |   |
|---|---|
|Detalles|Si el <xref:System.Xml.Linq.LoadOptions.SetLineInfo> valor se pasa al método Load y se produce un error de validación, el <xref:System.Xml.Schema.XmlSchemaException.LineNumber> y <xref:System.Xml.Schema.XmlSchemaException.LinePosition> contendrán ahora la información de línea.|
|Sugerencia|Código de control de excepciones que se da por supuesto <xref:System.Xml.Schema.XmlSchemaException.LineNumber> y <xref:System.Xml.Schema.XmlSchemaException.LinePosition> no estará conjunto debe actualizarse ya que estas propiedades ahora se establecerá correctamente cuando se usa SetLineInfo al cargar el XML.|
|Ámbito|Borde|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Xml.Linq.LoadOptions.SetLineInfo?displayProperty=nameWithType></li></ul>|

