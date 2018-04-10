### <a name="tabcontrol-selectionchanged-event-and-selectedcontent-property"></a>Propiedad de SelectedContent y TabControl SelectionChanged (evento)

|   |   |
|---|---|
|Detalles|A partir de .NET Framework 4.7.1, un <xref:System.Windows.Controls.TabControl> actualiza el valor de su <xref:System.Windows.Controls.TabControl.SelectedContent> propiedad antes de generar el <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> eventos cuando cambia su selección. 4.7 de .NET Framework y versiones anteriores, la actualización a SelectedContent ha ocurrido después del evento.|
|Sugerencia|Aplicaciones que se destinan a .NET Framework 4.7.1 o versiones posteriores pueden optar por esto cambiar y usar el comportamiento heredado mediante la adición de las siguientes acciones para la <code>&lt;runtime&gt;</code> sección del archivo de configuración de aplicación:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Aplicaciones destinadas a .NET Framework 4.7 o anterior pero se ejecutan en .NET Framework 4.7.1 o más adelante, puede habilitar el nuevo comportamiento agregando la siguiente línea a la <code>&lt;runtime&gt;</code> sección del archivo de .configuration de aplicación:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Ámbito|Secundaria|
|Versión|4.7.1|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.Windows.Controls.TabControl.SelectedContent?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.Selector.SelectionChanged?displayProperty=nameWithType></li></ul>|

