### <a name="signedxml-and-encryptedxml-breaking-changes"></a>SignedXml y EncryptedXml cambios importantes

|   |   |
|---|---|
|Detalles|En .NET Framework 4.6.2, revisiones de seguridad en <xref:System.Security.Cryptography.Xml.SignedXml?displayProperty=name> y <xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=name> conducir al diferentes comportamientos en tiempo de ejecución. Por ejemplo,<ul><li>Si un documento tiene varios elementos con el mismo <code>id</code> atributo y una firma está destinado a uno de esos elementos como la raíz de la firma, el documento ahora considerará no válido.</li><li>Documentos con algoritmos de transformación de XPath no canónico en referencias ahora se consideran no válidos.</li><li>Documentos con algoritmos de transformación XSLT no canónico en referencias están ahora considere la posibilidad de no válido.</li><li>Cualquier uso que hagan de programa de firmas de desconectado de un recurso externo podrá hacerlo.</li></ul>|
|Sugerencia|Los desarrolladores que desee consultar el uso de <xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform> y <xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform>, así como los tipos derivados de <xref:System.Security.Cryptography.Xml.Transform> puesto que un receptor de documento no pueda procesarlo.|
|Ámbito|Secundaria|
|Versión|4.6.2|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Security.Cryptography.Xml.Transform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXPathTransform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform?displayProperty=nameWithType></li></ul>|

