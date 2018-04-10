### <a name="scrolling-a-wpf-treeview-or-grouped-listbox-in-a-virtualizingstackpanel-can-cause-a-hang"></a>El desplazamiento de una vista de árbol de WPF o ListBox agrupado en un VirtualizingStackPanel puede producir una falta de respuesta

|   |   |
|---|---|
|Detalles|En v4.5 de .NET Framework, desplazamiento un WPF <xref:System.Windows.Controls.TreeView?displayProperty=name> en una pila virtualizada panel puede causar bloqueos si hay márgenes en la ventanilla (entre los elementos de la <xref:System.Windows.Controls.TreeView?displayProperty=name>, por ejemplo, o en un elemento ItemsPresenter). Además, en algunos casos, los elementos de diferentes tamaños de la vista pueden originar inestabilidad aun cuando no haya márgenes.|
|Sugerencia|Este error puede evitarse actualizando a .NET Framework 4.5.1. Como alternativa, se pueden quitar los márgenes de colecciones de vista (como <xref:System.Windows.Controls.TreeView?displayProperty=name>s) en la pila virtualizado paneles si todos los elementos contenidos son del mismo tamaño.|
|Ámbito|Major|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Windows.Controls.VirtualizingStackPanel.SetIsVirtualizing(System.Windows.DependencyObject,System.Boolean)?displayProperty=nameWithType></li></ul>|

