### <a name="deserialization-of-mailmessage-objects-serialized-under-the-net-framework-45-may-fail"></a>Puede producir un error de deserialización de objetos MailMessage serializados en .NET Framework 4.5

|   |   |
|---|---|
|Detalles|A partir de .NET Framework 4.5, <xref:System.Web.Mail.MailMessage> objetos pueden incluir caracteres no ASCII. En .NET Framework 4, solo se admiten caracteres ASCII. <xref:System.Web.Mail.MailMessage> objetos que contienen caracteres no ASCII y que se serializan en .NET Framework 4.5 o posterior no se puede deserializar en .NET Framework 4.|
|Sugerencia|Asegúrese de que el código proporciona el control de excepciones al deserializar un <xref:System.Web.Mail.MailMessage> objeto.|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Web.Mail.MailMessage?displayProperty=nameWithType></li></ul>|

