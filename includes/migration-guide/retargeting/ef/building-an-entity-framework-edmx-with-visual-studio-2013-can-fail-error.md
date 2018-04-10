### <a name="building-an-entity-framework-edmx-with-visual-studio-2013-can-fail-with-error-msb4062-if-using-the-entitydeploysplit-or-entityclean-tasks"></a>Compilar un edmx Entity Framework con Visual Studio 2013 puede producir un error MSB4062 si usa las tareas EntityDeploySplit o EntityClean

|   |   |
|---|---|
|Detalles|Herramientas de MSBuild 12.0 (incluidos en Visual Studio 2013) cambiado de ubicación de archivo de MSBuild, haciendo que los antiguos archivos de destino de Entity Framework no es válida. El resultado es un error de las tareas <code>EntityDeploySplit</code> y <code>EntityClean</code> debido a que no pueden buscar <code>Microsoft.Data.Entity.Build.Tasks.dll</code>. Tenga en cuenta que este salto debido a un cambio de conjunto de herramientas (MSBuild/VS), no es debido a un cambio de .NET Framework. Solo se producirá al actualizar las herramientas de desarrollo, no al actualizar únicamente .NET Framework.|
|Sugerencia|Archivos de destino de Entity Framework se corrigen para trabajar con el principio de diseño de MSBuild nueva en .NET Framework 4.6. Este problema se soluciona actualizando a esta versión de .NET Framework. También es posible usar [esta](http://stackoverflow.com/a/24249247/131944) solución alternativa para aplicar la revisión directamente a los archivos de destinos.|
|Ámbito|Major|
|Versión|4.5.1|
|Tipo|Redestinación|

