### <a name="soapformatter-cannot-deserialize-hashtable-and-similar-ordered-collection-objects"></a>SoapFormatter no puede deserializar la tabla hash y una ordenación similar objetos de colección

|   |   |
|---|---|
|Detalles|El <xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> hace no garantiza que los objetos serializan en una versión de .NET Framework se deserializará correctamente en una versión diferente. En concreto, algunas colecciones ordenan (como <xref:System.Collections.Hashtable?displayProperty=name>) agregado a los miembros entre 4.0 y 4.5, que no se pueden deserializar objetos de estos tipos con .NET 4.0 si se serializaron con .NET 4.5. Si los datos se serializaron y deserializaron con la misma versión de .NET Framework, no ocurrirá ningún problema.|
|Sugerencia|<xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> serialización debe reemplazarse por <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> serialización o <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> sea resistente a los cambios de .NET Framework.|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object,System.Runtime.Remoting.Messaging.Header[])?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream,System.Runtime.Remoting.Messaging.HeaderHandler)?displayProperty=nameWithType></li></ul>|

