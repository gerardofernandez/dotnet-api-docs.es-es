### <a name="sqlconnectionopen-fails-on-windows-7-with-non-ifs-winsock-bsp-or-lsp-present"></a>SqlConnection.Open produce un error en Windows 7 con IFS Winsock BSP o LSP presente

|   |   |
|---|---|
|Detalles|<xref:System.Data.SqlClient.SqlConnection.Open> y <xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)> producirá un error en .NET Framework 4.5, si se ejecuta en un equipo con Windows 7 con un IFS Winsock BSP o LSP está presente en el equipo. Para determinar si una no IFS BSP o LSP está instalado, use la <code>netsh WinSock Show Catalog</code> comando y examine cada <code>Winsock Catalog Provider Entry</code> elemento que se devuelve. Si el valor Service Flags tiene establecido el bit <code>0x20000</code>, el proveedor usa controladores IFS y funcionará correctamente. Si el bit <code>0x20000</code> está claro (no establecido), se trata de un BSP o LSP distinto de IFS.|
|Sugerencia|Este error se corrigió en .NET Framework 4.5.2, por lo que se puede evitar actualizando a una versión posterior de .NET Framework. También puede evitarse eliminando cualquier LSP de Winsock distinto de IFS que haya instalado.|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Data.SqlClient.SqlConnection.Open?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)?displayProperty=nameWithType></li></ul>|

