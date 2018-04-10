### <a name="applicationfiltermessage-no-longer-throws-for-re-entrant-implementations-of-imessagefilterprefiltermessage"></a>Application.FilterMessage ya no se produce para las implementaciones reentrantes de IMessageFilter.PreFilterMessage

|   |   |
|---|---|
|Detalles|Antes de .NET Framework 4.6.1, que realiza la llamada <xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)> con una <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)> que llama a <xref:System.Windows.Forms.Application.AddMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name> o <xref:System.Windows.Forms.Application.RemoveMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name> (mientras se también llama a <xref:System.Windows.Forms.Application.DoEvents>) produciría una <xref:System.IndexOutOfRangeException?displayProperty=name>. A partir de las aplicaciones dirigidas a .NET Framework 4.6.1, esta excepción ya no se produce y filtros reentrantes como se describió anteriormente pueden utilizarse.|
|Sugerencia|Tenga en cuenta que <xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)> ya no se iniciará para el que se vuelven a entrar <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)> comportamiento descrito anteriormente. Esto solo afecta a las aplicaciones dirigidas a la 4.6.1.Apps de .NET Framework como destino .NET Framework 4.6.1 pueden optar por este cambio (o destinatarios marcos anteriores pueden participar en las aplicaciones) mediante la [DontSupportReentrantFilterMessage](~/docs/framework/migration-guide/mitigation-custom-imessagefilter-prefiltermessage-implementations.md#mitigation) modificador de compatibilidad.|
|Ámbito|Borde|
|Versión|4.6.1|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)?displayProperty=nameWithType></li></ul>|

