### <a name="data-written-to-printsystemjobinfojobstream-must-be-in-xps-format"></a>Datos escritos en PrintSystemJobInfo.JobStream deben estar en formato XPS

|   |   |
|---|---|
|Detalles|El <xref:System.Printing.PrintSystemJobInfo.JobStream> propiedad expone el flujo de trabajo de impresión. El usuario puede enviar datos sin formato a los componentes de impresión del sistema operativo subyacente mediante la escritura a esta secuencia. A partir de .NET Framework 4.5 en Windows 8 y versiones posteriores del sistema operativo Windows, escritos en esta secuencia de datos deben estar en formato XPS como una secuencia de paquete.|
|Sugerencia|Para mostrar contenido de impresión, puede realizar una de las acciones siguientes:<ul><li>Utilice la clase <xref:System.Windows.Xps.XpsDocumentWriter> para mostrar contenido de impresión. Esta es la alternativa recomendada.</li><li>Asegúrese de que los datos enviados a la secuencia devuelta por la <xref:System.Printing.PrintSystemJobInfo.JobStream> propiedad está en formato XPS como una secuencia de paquete.</li></ul>|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Printing.PrintSystemJobInfo.JobStream?displayProperty=nameWithType></li></ul>|

