### <a name="item-scrolling-a-flat-list-with-items-of-different-pixel-height"></a>Desplazamiento de elemento de una lista plana con elementos de alto de píxel diferente

|   |   |
|---|---|
|Detalles|Cuando un <xref:System.Windows.Controls.ItemsControl?displayProperty=name> muestra una colección con la virtualización (<code>IsVirtualizing=true</code>) y el elemento - desplazamiento (<code>ScrollUnit=Item</code>), y cuando se desplaza el control para mostrar un elemento cuyo alto en píxeles difiere de sus vecinos, la <xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name> recorre en iteración todos los elementos de la colección. La interfaz de usuario no responde durante esta iteración; Si la colección es grande, esto se puede percibir como una falta de respuesta. La iteración se produce en otras circunstancias, incluso en las versiones anteriores. NET. Por ejemplo, se produce al desplazarse por el píxel (<code>ScrollUnit=Pixel</code>) al encontrar un elemento con el alto de píxel diferente y al desplazarse por el elemento de datos jerárquicos (como un <xref:System.Windows.Controls.TreeView?displayProperty=name> o <xref:System.Windows.Controls.ItemsControl?displayProperty=name> con agrupación habilitado) al encontrar un elemento con un número diferente de elementos descendientes a sus vecinos. En el caso de alto en píxeles de desplazamiento de elemento y diferentes, la iteración se introdujo en .net 4.6.1 para corregir errores en el diseño de los datos jerárquicos.  No se necesita si los datos son planos (sin jerarquía) y .net 4.6.2 no lo hace en ese caso.|
|Sugerencia|Si la iteración se produce en .net 4.6.1 pero no en las versiones anteriores: es decir, si la <xref:System.Windows.Controls.ItemsControl?displayProperty=name> es una lista plana de desplazamiento de elemento, con elementos de alto de píxel diferentes: existen dos soluciones:<ol><li>Instale .net 4.6.2.</li><li>Instale la revisión 1605 de recursos humanos para .net 4.6.1.</li></ol>|
|Ámbito|Secundaria|
|Versión|4.6.1|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=nameWithType></li></ul>|

