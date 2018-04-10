### <a name="gridviews-with-allowcustompaging-set-to-true-may-fire-the-pageindexchanging-event-when-leaving-the-final-page-of-the-view"></a>GridView con AllowCustomPaging establecido en true puede desencadenar el evento de PageIndexChanging al salir de la página final de la vista

|   |   |
|---|---|
|Detalles|Hace que un error en .NET Framework 4.5 <xref:System.Web.UI.WebControls.GridView.PageIndexChanging?displayProperty=name> a veces no se active para <xref:System.Web.UI.WebControls.GridView?displayProperty=name>s que ha habilitado <xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=name>.|
|Sugerencia|Este problema se ha solucionado en .NET Framework 4.6 y puede solucionarse al actualizar a esa versión de .NET Framework. Como una solución alternativa, la aplicación puede hacer un BindGrid explícita en cualquier <code>Page_Load</code> que alcanzaba estas condiciones (la <xref:System.Web.UI.WebControls.GridView?displayProperty=name> está en la última página y última<xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name> es diferente de <xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name>). Como alternativa, la aplicación puede modificarse para permitir la paginación (en lugar de la paginación personalizada), como ese escenario no muestra el problema.|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=nameWithType></li></ul>|

