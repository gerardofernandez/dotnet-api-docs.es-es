### <a name="wpf-datatemplate-elements-are-now-visible-to-uia"></a>Elementos de plantilla de datos de WPF ahora son visibles para UIA

|   |   |
|---|---|
|Detalles|Anteriormente, <xref:System.Windows.DataTemplate?displayProperty=name> elementos estaban visibles para la automatización de la interfaz de usuario. A partir de la versión 4.5, la automatización de la IU detectará estos elementos. Esto es útil en muchos casos, pero puede interrumpir las pruebas que dependen de los árboles UIA que no contenga <xref:System.Windows.DataTemplate?displayProperty=name> elementos.|
|Sugerencia|Pruebas de automatización de la interfaz de usuario para esta aplicación puede necesitar actualizan para tener en cuenta para el árbol UIA ahora incluyen previamente invisible <xref:System.Windows.DataTemplate?displayProperty=name> elementos. Por ejemplo, en aquellas pruebas en las que se espere que haya ciertos elementos contiguos entre sí, ahora puede ser necesario esperar ciertos elementos intermedios de la UIA que antes no eran visibles. También puede ser necesario actualizar con nuevos valores pruebas que dependan de ciertos recuentos o índices para elementos de la UIA.|
|Ámbito|Borde|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Windows.DataTemplate.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.DataTemplate.%23ctor(System.Object)?displayProperty=nameWithType></li></ul>|

