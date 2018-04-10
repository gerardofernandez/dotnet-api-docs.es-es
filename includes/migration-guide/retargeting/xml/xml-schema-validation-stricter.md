### <a name="xml-schema-validation-is-stricter"></a>Validación de esquemas XML es más estricta

|   |   |
|---|---|
|Detalles|En .NET Framework 4.5, la validación de esquemas XML es más estricta. Si usa xsd:anyURI para validar un identificador URI, como un protocolo mailto, la validación producirá un error si hay espacios en el URI. En versiones anteriores de .NET Framework, la validación se realizaba correctamente. El cambio sólo afecta a aplicaciones que tienen como destino .NET Framework 4.5.|
|Sugerencia|Si es necesaria la validación más flexible de .NET Framework 4.0, la aplicación de validación puede tener como destino versión 4.0 de .NET Framework. Cuando de redestinación en .NET 4.5, sin embargo, la revisión de código se debe realizar para asegurarse de que el URI no válido (con espacios en blanco) no se esperan como valores de atributo con el tipo de datos anyURI.|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Redestinación|

