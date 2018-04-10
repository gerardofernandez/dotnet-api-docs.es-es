### <a name="calling-itemsrefresh-on-a-wpf-listbox-listview-or-datagrid-with-items-selected-can-cause-duplicate-items-to-appear-in-the-element"></a>Llamar a Items.Refresh en un cuadro de lista de WPF, ListView o DataGrid con los elementos seleccionados pueden hacer que los elementos duplicados que aparezca en el elemento

|   |   |
|---|---|
|Detalles|En .NET Framework 4.5, llamar a ListBox.Items.Refresh desde el código mientras se seleccionan elementos en un <xref:System.Windows.Controls.ListBox?displayProperty=name> puede hacer que los elementos seleccionados se duplique en la lista. Se produce un problema similar con <xref:System.Windows.Controls.ListView?displayProperty=name> y <xref:System.Windows.Controls.DataGrid?displayProperty=name>. Este problema se corrigió en .NET Framework 4.6.|
|Sugerencia|Este problema puede puede solucionarse mediante programación anulando la selección de elementos antes de <xref:System.Windows.Data.CollectionView.Refresh?displayProperty=name> se llama y, a continuación, volver a ello, selecciónelos después de que se complete la llamada. Este problema se resolvió en .NET Framework 4.6, por lo que otra posible solución es actualizar a esta versión de .NET Framework.|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Windows.Data.CollectionView.Refresh?displayProperty=nameWithType></li></ul>|

