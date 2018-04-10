### <a name="some-workflow-drag-and-drop-apis-are-obsolete"></a>Algunas API de arrastrar y colocar de flujo de trabajo está obsoleto

|   |   |
|---|---|
|Detalles|Esta API de arrastrar y colocar de flujo de trabajo está obsoleta y hará que las advertencias del compilador si se vuelve a generar la aplicación en 4.5.|
|Sugerencia|Nueva <xref:System.Activities.Presentation.DragDropHelper?displayProperty=name> API que admiten operaciones con varios objetos deben usarse en su lugar. También es posible suprimir las advertencias de compilación o usar un compilador anterior para evitarlas. Las API siguen siendo compatibles.|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.Activities.Presentation.DragDropHelper.DoDragMove(System.Activities.Presentation.WorkflowViewElement,System.Windows.Point)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetCompositeView(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDraggedModelItem(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDroppedObject(System.Windows.DependencyObject,System.Windows.DragEventArgs,System.Activities.Presentation.EditingContext)?displayProperty=nameWithType></li></ul>|

