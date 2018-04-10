### <a name="datagridcellspanelbringindexintoview-throws-argumentoutofrangeexception"></a>DataGridCellsPanel.BringIndexIntoView produce ArgumentOutOfRangeException

|   |   |
|---|---|
|Detalles|<xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> funcionará asincrónicamente cuando está habilitada la virtualización de la columna, pero los anchos de columna no se ha determinado todavía.  Si las columnas se quitan antes de que ocurra el trabajo asincrónico, un <xref:System.ArgumentOutOfRangeException?displayProperty=name> puede producirse.|
|Sugerencia|Cualquiera de las siguientes acciones:<ol><li>Actualización a .NET 4.7.</li><li>Instale la revisión de servicio más reciente para .NET 4.6.2.</li><li>Evitar la eliminación de columnas hasta que la respuesta asincrónica a <xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> se ha completado.</li></ol>|
|Ámbito|Borde|
|Versión|4.6.2|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object,System.Windows.Controls.DataGridColumn)?displayProperty=nameWithType></li></ul>|

