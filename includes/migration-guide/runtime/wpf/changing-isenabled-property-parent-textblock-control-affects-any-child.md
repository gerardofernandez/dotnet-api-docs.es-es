### <a name="changing-the-isenabled-property-of-the-parent-of-a-textblock-control-affects-any-child-controls"></a>Cambiar la propiedad IsEnabled del elemento primario de un control TextBlock afecta a todos los controles secundarios

|   |   |
|---|---|
|Detalles|A partir de .NET Framework 4.6.2, cambiar el <xref:System.Windows.UIElement.IsEnabled?displayProperty=name> propiedad del elemento primario de un <xref:System.Windows.Controls.TextBlock?displayProperty=name> control afecta a todos los controles secundarios (por ejemplo, los hipervínculos y los botones) de la <xref:System.Windows.Controls.TextBlock?displayProperty=name> control. En .NET Framework 4.6.1 y versiones anteriores, se controla dentro de un <xref:System.Windows.Controls.TextBlock?displayProperty=name> no siempre refleja el estado de la <xref:System.Windows.UIElement.IsEnabled?displayProperty=name> propiedad de la <xref:System.Windows.Controls.TextBlock?displayProperty=name> primario.|
|Sugerencia|Ninguno. Este cambio se ajusta al comportamiento esperado de los controles dentro de un control <xref:System.Windows.Controls.TextBlock?displayProperty=name>.|
|Ámbito|Secundaria|
|Versión|4.6.2|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Windows.UIElement.IsEnabled?displayProperty=nameWithType></li></ul>|

