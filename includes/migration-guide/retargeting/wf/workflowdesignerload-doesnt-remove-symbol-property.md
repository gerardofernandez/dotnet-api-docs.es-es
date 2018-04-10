### <a name="workflowdesignerload-doesnt-remove-symbol-property"></a>WorkflowDesigner.Load no quita la propiedad de símbolo

|   |   |
|---|---|
|Detalles|Cuando el destino es .NET Framework 4.5 en el Diseñador de flujo de trabajo y cargar un flujo de trabajo 3.5 RE-hospedado con el <xref:System.Activities.Presentation.WorkflowDesigner.Load> método, un <xref:System.Xaml.XamlDuplicateMemberException?displayProperty=name> se produce al guardar el flujo de trabajo.|
|Sugerencia|Este error sólo se presenta cuando el destino es .NET Framework 4.5 en el Diseñador de flujo de trabajo, por lo que puede ser solucionado estableciendo la <code>WorkflowDesigner.Context.Services.GetService&lt;DesignerConfigurationService&gt;().TargetFrameworkName</code> a la Framework.Alternatively .NET 4.0, el problema puede evitarse mediante el uso de la <xref:System.Activities.Presentation.WorkflowDesigner.Load(System.String)> método para cargar el flujo de trabajo en lugar de <xref:System.Activities.Presentation.WorkflowDesigner.Load>.|
|Ámbito|Major|
|Versión|4.5|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.Activities.Presentation.WorkflowDesigner.Load?displayProperty=nameWithType></li></ul>|

