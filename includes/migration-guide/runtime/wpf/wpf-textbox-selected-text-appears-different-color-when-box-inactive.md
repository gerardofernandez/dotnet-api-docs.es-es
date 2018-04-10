### <a name="wpf-textbox-selected-text-appears-a-different-color-when-the-text-box-is-inactive"></a>Texto de cuadro de texto de WPF seleccionado aparece un color diferente cuando el cuadro de texto está inactivo

|   |   |
|---|---|
|Detalles|En .NET 4.5, cuando un control de cuadro de texto de WPF esté inactivo (sin el foco), el texto seleccionado dentro del cuadro aparecerá en un color diferente al que lo haría con el control activo.|
|Sugerencia|Comportamiento de (.NET 4.0) anterior puede restaurarse estableciendo la <xref:System.Windows.FrameworkCompatibilityPreferences.AreInactiveSelectionHighlightBrushKeysSupported> propiedad <code>false</code>.|
|Ámbito|Borde|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

