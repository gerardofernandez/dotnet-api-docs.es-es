### <a name="missing-target-framework-moniker-results-in-40-behavior"></a>Resultados de Moniker de la plataforma de destino que faltan en el comportamiento de 4.0

|   |   |
|---|---|
|Detalles|Las aplicaciones sin un <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> aplicados en el ensamblado nivel ejecutará automáticamente usando la semántica (estándar) de .NET Framework 4.0. Para asegurarse de alta calidad, se recomienda que todos los archivos binarios se atribuir explícitamente con un <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> que indica la versión de .NET Framework que se compilaron. Tenga en cuenta que al utilizar un moniker de la plataforma de destino en un archivo de proyecto hará que MSBuild aplicar automáticamente un <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>.|
|Sugerencia|A <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> debe especificarse, ya sea a través de agregar el atributo directamente al ensamblado o mediante la especificación de una plataforma de destino en la [archivo de proyecto o a través de Visual Studio GUI de propiedades del proyecto](http://blogs.msdn.com/b/visualstudio/archive/2010/05/19/visual-studio- managed-multi-targeting-part-1-concepts-target-framework-moniker-target-framework.aspx).|
|Ámbito|Major|
|Versión|4.5|
|Tipo|Tiempo de ejecución|

