### <a name="xslt-forward-compat-now-works"></a>Ahora funciona correctamente la compatibilidad directa de XSLT

|   |   |
|---|---|
|Detalles|En .NET Framework 4, compatibilidad con versiones de XSLT 1.0 presentaba los siguientes problemas:<ul><li>La carga de una hoja de estilos no se realizaba correctamente si su versión estaba establecida en 2.0 y el analizador encontraba una construcción de XSLT 1.0 desconocida.</li><li>La construcción <code>xsl:sort</code> no podía ordenar los datos si la versión de la hoja de estilos estaba establecida en 1.1.</li></ul>En .NET Framework 4.5, estos problemas se han solucionado y modo de compatibilidad con versiones posteriores de XSLT 1.0 funciona correctamente.|
|Sugerencia|Mayoría de las aplicaciones debe ser afectada, pero los datos se ordenarán forma distinta en algunos casos ahora que se respeta xsl: Sort. Si <code>xsl:sort</code> es utilizada en 1.1 hojas de estilo, confirme que las aplicaciones no se según el orden de los datos sin ordenar. Si las aplicaciones se basan en el comportamiento de ordenación de 4.0, quitar <code>xsl:sort</code> desde la hoja de estilos.|
|Ámbito|Borde|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform?displayProperty=nameWithType></li></ul>|

