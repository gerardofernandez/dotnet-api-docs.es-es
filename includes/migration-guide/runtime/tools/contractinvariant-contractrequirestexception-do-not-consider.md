### <a name="contractinvariant-or-contractrequirestexception-do-not-consider-stringisnullorempty-to-be-pure"></a>Contract.Invariant o Contract.Requires<TException> no se tienen en cuenta String.IsNullOrEmpty para ser puros

|   |   |
|---|---|
|Detalles|Para las aplicaciones que tienen como destino .NET Framework 4.6.1, si el nombre invariable del contrato para <xref:System.Diagnostics.Contracts.Contract.Invariant%2A?displayProperty=nameWithType> o el contrato de condición previa para <xref:System.Diagnostics.Contracts.Contract.Requires%2A?displayProperty=nameWithType)> llamadas el <xref:System.String.IsNullOrEmpty%2A?displayProperty=nameWithType> método, el sistema de reescritura emite la advertencia CC1036 del compilador: &quot;detecta la llamada al método ' System.String.IsNullOrWhteSpace(System.String)' sin [puro] en el método.&quot; Se trata de una advertencia en lugar de un error del compilador del compilador.|
|Sugerencia|Este comportamiento se solucionó en [Problema de GitHub #339](https://github.com/Microsoft/CodeContracts/issues/339). Para eliminar esta advertencia, puede descargar y compilar una versión actualizada del código fuente para la herramienta de contratos de código de [GitHub](https://github.com/Microsoft/CodeContracts/blob/master/README.md). La información de descarga se encuentra en la parte inferior de la página.|
|Ámbito|Secundaria|
|Versión|4.6.1|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Diagnostics.Contracts.Contract.Invariant(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Contracts.Contract.Requires(System.Boolean)?displayProperty=nameWithType></li></ul>|

