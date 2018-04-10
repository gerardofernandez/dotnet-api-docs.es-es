### <a name="netdatacontractserializer-fails-to-deserialize-a-concurrentdictionary-serialized-with-a-different-net-version"></a>No se puede deserializar ConcurrentDictionary serializado con una versión diferente de .NET NetDataContractSerializer

|   |   |
|---|---|
|Detalles|De forma predeterminada, el <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> puede usarse sólo si tanto la serialización y deserialización de extremos comparten los mismos tipos CLR. Por lo tanto, no se garantiza que se puede deserializar un objeto serializado con una versión de .NET Framework con una versión diferente.<xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> es un tipo que es conocido en no para deserializar correctamente si con .NET Framework 4.5 o versiones anteriores a serializar y deserializar con .NET Framework 4.5.1 o posterior.|
|Sugerencia|Hay una serie de soluciones posibles para este problema:<ul><li>Actualice el equipo para que use .NET Framework 4.5.1, también serializar.</li><li>Use <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> en lugar de <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> como esto no cuenta con los mismos tipos CLR exactos en serializar y deserializar los extremos.</li><li>Use <xref:System.Collections.Generic.Dictionary%602?displayProperty=name> en lugar de <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> puesto que no muestran este 4.5 determinado -&gt;interrumpir 4.5.1.</li></ul>|
|Ámbito|Secundaria|
|Versión|4.5.1|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Runtime.Serialization.NetDataContractSerializer.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li></ul>|

