### <a name="a-concurrentdictionary-serialized-in-net-45-with-netdatacontractserializer-cannot-be-deserialized-by-net-451-or-452"></a>No se puede deserializar ConcurrentDictionary serializado en .NET 4.5 con NetDataContractSerializer por .NET 4.5.1 o 4.5.2

|   |   |
|---|---|
|Detalles|Debido a cambios internos para el tipo, <xref:System.Collections.Concurrent.ConcurrentDictionary%602> objetos que se serializan con .NET Framework 4.5 con el <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> no se puede deserializar en .NET Framework 4.5.1 o en la 4.5.2.Note de .NET Framework es móvil en el otro (dirección serializar con .NET Framework 4.5 y deserializar con .NET Framework 4.5) funciona. Del mismo modo, toda la serialización entre versiones 4.x funciona con el 4.6.Serializing de .NET Framework y no se ve afectado el deserializar con una única versión de .NET Framework.|
|Sugerencia|Si es necesario serializar y deserializar un <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> entre el .NET Framework 4.5 y .NET Framework 4.5.1/4.5.2, un serializador alternativo, como el <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> o <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> serializador debe usarse en lugar de la <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>. O bien, porque se trata este problema en .NET Framework 4.6, quizás se puedan resolver mediante la actualización a esa versión de .NET Framework.|
|Ámbito|Secundaria|
|Versión|4.5.1|
|Tipo|Tiempo de ejecución|

