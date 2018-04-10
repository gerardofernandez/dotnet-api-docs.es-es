### <a name="assemblies-compiled-with-regexcompiletoassembly-breaks-between-40-and-45"></a>Ensamblados compilados con saltos de Regex.CompileToAssembly entre 4.0 y 4.5

|   |   |
|---|---|
|Detalles|Si un ensamblado de expresiones regulares compiladas se crea con el destino .NET Framework 4 pero con .NET Framework 4.5, intenta usar una de las expresiones regulares en que instala el ensamblado en un sistema de .NET Framework 4 produce una excepción.|
|Sugerencia|Para evitar este problema, realice una de las acciones siguientes:<ul><li>Compile el ensamblado que contiene las expresiones regulares de .NET Framework 4.</li><li>Use una expresión regular interpretada.</li></ul>|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName)?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[])?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[],System.String)?displayProperty=nameWithType></li></ul>|

