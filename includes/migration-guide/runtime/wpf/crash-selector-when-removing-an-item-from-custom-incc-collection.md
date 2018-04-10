### <a name="crash-in-selector-when-removing-an-item-from-a-custom-incc-collection"></a>Al quitar un elemento de una colección personalizada de INCC de bloqueos en Selector

|   |   |
|---|---|
|Detalles|Un <code>T:System.InvalidOperationException</code> puede producirse en el siguiente escenario:<ul><li>El ItemsSource para un <code>T:System.Windows.Controls.Primitives.Selector</code> es una colección con una implementación personalizada de <code>T:System.Collections.Specialized.INotifyCollectionChanged</code>.</li><li>El elemento seleccionado se quitará de la colección.</li><li>El <code>T:System.Collections.Specialized.NotifyCollectionChangedEventArgs</code> tiene <code>P:System.Collections.Specialized.NotifyCollectionChangedEventArgs.OldStartingIndex</code> = -1 (lo que indica una posición desconocida).</li></ul>Pila de llamadas de la excepción que se inicia en System.Windows.Threading.Dispatcher.VerifyAccess() en System.Windows.DependencyObject.GetValue (DependencyProperty dp) en System.Windows.Controls.Primitives.Selector.GetIsSelected (DependencyObject elemento) esta excepción puede producirse en .net 4.5, si la aplicación tiene más de un subproceso Dispatcher. En .net 4.7 la excepción también puede producirse en las aplicaciones con un único subproceso de distribuidor. El problema se corregirá en .net 4.7.1.|
|Sugerencia|Actualización a .net 4.7.1.|
|Ámbito|Secundaria|
|Versión|4.7|
|Tipo|Tiempo de ejecución|

