### <a name="itemsclear-does-not-remove-duplicates-from-selecteditems"></a>Items.Clear no quitar duplicados de SelectedItems

|   |   |
|---|---|
|Detalles|Supongamos que un Selector (con la selección múltiple habilitado) tiene duplicados su <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> recopilación: el mismo elemento aparece más de una vez.  Quitar los elementos del origen de datos (por ejemplo, mediante una llamada a Items.Clear) no se puede quitar <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>; solo se quita la primera instancia. Además, su uso posterior de <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> (p. ej. SelectedItems.Clear()) pueden experimentar problemas como <xref:System.ArgumentException?displayProperty=name>, porque <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> contiene elementos que ya no están en el origen de datos.|
|Sugerencia|Si es posible actualizar a .NET 4.6.2.|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=nameWithType></li></ul>|

