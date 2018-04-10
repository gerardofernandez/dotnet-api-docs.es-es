### <a name="calling-datagridcommitedit-from-a-celleditending-handler-drops-focus"></a>Llamar a DataGrid.CommitEdit desde un controlador de CellEditEnding quita el foco

|   |   |
|---|---|
|Detalles|Al llamar a <xref:System.Windows.Controls.DataGrid.CommitEdit> desde uno de los <xref:System.Windows.Controls.DataGrid?displayProperty=name>del <xref:System.Windows.Controls.DataGrid.CellEditEnding?displayProperty=name> hace que los controladores de eventos el <xref:System.Windows.Controls.DataGrid?displayProperty=name> pierde el foco.|
|Sugerencia|Este error se corrigió en .NET Framework 4.5.2, por lo que se puede evitar actualizando a una versión posterior de .NET Framework. Como alternativa, se puede evitar volviendo a seleccionar explícitamente la <xref:System.Windows.Controls.DataGrid?displayProperty=name> después de llamar a <xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=name>.|
|Ámbito|Borde|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.CommitEdit(System.Windows.Controls.DataGridEditingUnit,System.Boolean)?displayProperty=nameWithType></li></ul>|

