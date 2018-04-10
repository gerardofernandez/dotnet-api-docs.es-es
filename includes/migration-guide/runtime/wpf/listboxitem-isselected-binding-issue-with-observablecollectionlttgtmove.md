### <a name="listboxitem-isselected-binding-issue-with-observablecollectionlttgtmove"></a>Problema de enlace de ListBoxItem IsSelected con ObservableCollection&lt;T&gt;. Mover

|   |   |
|---|---|
|Detalles|Al llamar a <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> o <xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)> en una colección enlazada a un <xref:System.Windows.Controls.ListBox?displayProperty=name> con los elementos seleccionados puede provocar un comportamiento incorrecto con selección futuras o unselection de <xref:System.Windows.Controls.ListBox?displayProperty=name> elementos.|
|Sugerencia|Al llamar a <xref:System.Collections.ObjectModel.Collection%601.Remove(%600)?displayProperty=name> y <xref:System.Collections.ObjectModel.Collection%601.Insert(System.Int32,%600)?displayProperty=name> en lugar de <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> funcionará alternativa a este problema. Este problema se resolvió en .NET Framework 4.6, por lo que otra posible solución es actualizar a esta versión de .NET Framework.|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)?displayProperty=nameWithType></li><li><xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)?displayProperty=nameWithType></li></ul>|

