### <a name="intermittently-unable-to-scroll-to-bottom-item-in-itemscontrols-like-listbox-and-datagrid-when-using-custom-datatemplates"></a>No puede desplazarse al elemento de la parte inferior de ItemsControls (por ejemplo, cuadro de lista y cuadrícula de datos) de forma intermitente al usar DataTemplates personalizado

|   |   |
|---|---|
|Detalles|En algunos casos, un error en .NET Framework 4.5 está causando ItemsControls (como <xref:System.Windows.Controls.ListBox?displayProperty=name>, <xref:System.Windows.Controls.ComboBox?displayProperty=name>, <xref:System.Windows.Controls.DataGrid?displayProperty=name>, etc.) no desplazarse a su elemento de la parte inferior al usar DataTemplates personalizado. Si se trata de efectuar el desplazamiento una segunda vez (después de haber vuelto arriba), sí funciona.|
|Sugerencia|Este problema se resolvió en .NET Framework 4.5.2, por lo que otra posible solución es actualizar a esta versión (u otra posterior) de .NET Framework. Los usuarios también pueden arrastrar las barras de desplazamiento hasta los últimos elementos de estas colecciones, pero puede ser posible que tengan que hacerlo dos veces para conseguirlo.|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Tiempo de ejecución|

