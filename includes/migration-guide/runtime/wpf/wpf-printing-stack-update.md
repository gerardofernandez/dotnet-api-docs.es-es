### <a name="wpf-printing-stack-update"></a>Actualización de la pila WPF impresión

|   |   |
|---|---|
|Detalles|Uso de las API de impresión de WPF <xref:System.Printing.PrintQueue?displayProperty=name> ahora llamar a API de paquete de documento de impresión de la ventana en favor de la API de impresión XPS ya en desuso. El cambio se realizó con capacidad de servicio en cuenta; los usuarios ni a los desarrolladores deberían ver los cambios de comportamiento o el uso de la API. La nueva pila de impresión está habilitada de forma predeterminada cuando se ejecuta en Windows 10 creadores de actualización. La pila de impresión antigua sigue continuarán funcionando igual que antes en versiones anteriores de Windows.|
|Sugerencia|Para usar la pila antigua en Windows 10 creadores de actualización, establezca la <code>UseXpsOMPrinting</code> valor REG_DWORD de la <code>HKEY_CURRENT_USER\Software\Microsoft\.NETFramework\Windows Presentation Foundation\Printing</code> clave del registro para <code>1</code>.|
|Ámbito|Borde|
|Versión|4.7|
|Tipo|Tiempo de ejecución|

