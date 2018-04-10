### <a name="workflow-now-throws-original-exception-instead-of-nullreferenceexception-in-some-cases"></a>Flujo de trabajo ahora produce la excepción original en lugar de excepciones NullReferenceException en algunos casos

|   |   |
|---|---|
|Detalles|En .NET Framework 4.6.2 y versiones anteriores, cuando el método de ejecución de una actividad de flujo de trabajo produce una excepción con un <code>null</code> valor para el <xref:System.Exception.Message> propiedad, el tiempo de ejecución de flujo de trabajo de System.Activities produce una <xref:System.NullReferenceException?displayProperty=name>, máscara el excepción original. En el 4.7 de Framework. NET, se produce la excepción previamente enmascarada.|
|Sugerencia|Si el código se basa en el control de la <xref:System.NullReferenceException?displayProperty=name>, cámbielo para detectar las excepciones que pueden producirse desde sus actividades personalizadas.|
|Ámbito|Secundaria|
|Versión|4.7|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Activities.CodeActivity.Execute(System.Activities.CodeActivityContext)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity%601.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.WorkflowInvoker.Invoke?displayProperty=nameWithType></li></ul>|

