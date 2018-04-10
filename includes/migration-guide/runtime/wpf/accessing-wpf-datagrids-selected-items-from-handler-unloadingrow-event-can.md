### <a name="accessing-a-wpf-datagrids-selected-items-from-a-handler-of-the-datagrids-unloadingrow-event-can-cause-a-nullreferenceexception"></a>Obtiene acceso a los elementos seleccionados de un control DataGrid de WPF desde un controlador de eventos de UnloadingRow del control DataGrid puede producir una excepción NullReferenceException

|   |   |
|---|---|
|Detalles|Debido a un error de .NET Framework 4.5, controladores de eventos para <xref:System.Windows.Controls.DataGrid> eventos que implica la eliminación de una fila pueden provocar un <xref:System.NullReferenceException?displayProperty=name> que se produce si tienen acceso a la <xref:System.Windows.Controls.DataGrid>del <xref:System.Windows.Controls.Primitives.Selector.SelectedItem?displayProperty=name> o <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> propiedades.|
|Sugerencia|Este problema se ha solucionado en .NET Framework 4.6 y puede solucionarse al actualizar a esa versión de .NET Framework.|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Windows.Controls.DataGrid.UnloadingRow?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.UnloadingRowDetails?displayProperty=nameWithType></li></ul>|

