### <a name="marshalsizeof-and-marshalptrtostructure-overloads-break-dynamic-code"></a>Marshal.SizeOf y sobrecargas de método Marshal.PtrToStructure interrumpir el código dinámico

|   |   |
|---|---|
|Detalles|A partir de .NET Framework 4.5.1, enlazar dinámicamente a los métodos <xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601>, <xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601(%60%600)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Object)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Type)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr)>, o <xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr,%60%600)>, (a través de Windows PowerShell, IronPython o el C# palabra clave dinámica, por ejemplo) puede dar lugar a <code>MethodInvocationExceptions</code> porque se han agregado nuevas sobrecargas de estos métodos que pueden ser ambigua para los motores de scripting.|
|Sugerencia|Actualizar los scripts para indicar claramente qué sobrecarga debe usarse. Normalmente, puede hacerse convirtiendo de forma explícita los parámetros de tipo del método como <xref:System.Type>. Visite [este vínculo](https://support.microsoft.com/kb/2909958/) para consultar información más detallada y ejemplos de soluciones alternativas para este problema.|
|Ámbito|Secundaria|
|Versión|4.5.1|
|Tipo|Tiempo de ejecución|

