### <a name="entity-framework-version-must-match-the-net-framework-version"></a>Versión de Entity Framework debe coincidir con la versión de .NET Framework

|   |   |
|---|---|
|Detalles|La versión de entity framework debe coincidir con la versión de .NET framework. Entity Framework 5 se recomienda para .NET 4.5. Hay algunos problemas conocidos con EF 4.x en un proyecto de .NET 4.5 alrededor de <xref:System.ComponentModel.DataAnnotations>. En .NET 4.5, estos se movieron a un ensamblado diferente, por lo que hay problemas de determinar qué las anotaciones que se va a usar.|
|Sugerencia|Actualización a Entity Framework 5 para .NET Framework 4.5|
|Ámbito|Major|
|Versión|4.5|
|Tipo|Redestinación|

