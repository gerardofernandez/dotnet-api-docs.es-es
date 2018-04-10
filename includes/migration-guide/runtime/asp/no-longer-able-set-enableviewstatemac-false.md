### <a name="no-longer-able-to-set-enableviewstatemac-to-false"></a>Ya no se puede establecer EnableViewStateMac en false

|   |   |
|---|---|
|Detalles|ASP.NET ya no permite a los desarrolladores especificar <code>&lt;pages enableViewStateMac=&quot;false&quot;/&gt;</code> o <code>&lt;@Page EnableViewStateMac=&quot;false&quot; %&gt;</code>. El código de autenticación de mensajes (MAC) de estado de vista ahora es obligatorio para todas las solicitudes con estado de vista integrado. Solo las aplicaciones que establezca explícitamente la propiedad EnableViewStateMac en <code>false</code> se ven afectados.|
|Sugerencia|Se debe suponer EnableViewStateMac se establezca en true y se debe resolver cualquier error resultante de MAC (como se explica en [esta guía](https://support.microsoft.com/kb/2915218), que contiene varias resoluciones según las particularidades de cuál es la causa errores de MAC).|
|Ámbito|Major|
|Versión|4.5.2|
|Tipo|Tiempo de ejecución|

