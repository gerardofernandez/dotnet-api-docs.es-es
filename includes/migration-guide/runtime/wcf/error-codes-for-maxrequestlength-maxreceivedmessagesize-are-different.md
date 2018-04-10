### <a name="error-codes-for-maxrequestlength-or-maxreceivedmessagesize-are-different"></a>Códigos de error para maxRequestLength o maxReceivedMessageSize son diferentes

|   |   |
|---|---|
|Detalles|Mensajes de WCF servicios web hospedados en Internet Information Services (IIS) o servidor de desarrollo de ASP.NET que superan maxRequestLength (en ASP.NET) o maxReceivedMessageSize (en WCF) tiene otro error código de estado HTTP de código de esquemaLos ha cambiado de 400 (solicitud incorrecta ) a 413 (entidad de solicitud demasiado grande) y los mensajes que superan el atributo maxRequestLength o el valor de maxReceivedMessageSize producir un <xref:System.ServiceModel.ProtocolException?displayProperty=name> excepción. Esto incluye los casos en que se transmite por secuencias el modo de transferencia.|
|Sugerencia|Este cambio facilita la depuración en casos donde la longitud del mensaje supera los límites permitidos por ASP.NET o WCF. Debe modificar cualquier código que realiza el procesamiento basándose en un código de estado HTTP 400.|
|Ámbito|Borde|
|Versión|4.5|
|Tipo|Tiempo de ejecución|

