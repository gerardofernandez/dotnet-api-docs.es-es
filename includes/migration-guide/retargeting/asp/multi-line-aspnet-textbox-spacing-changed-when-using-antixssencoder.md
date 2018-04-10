### <a name="multi-line-aspnet-textbox-spacing-changed-when-using-antixssencoder"></a>Espaciado de cuadro de texto de ASP.Net de varias líneas cambiado cuando se use AntiXSSEncoder

|   |   |
|---|---|
|Detalles|En .NET Framework 4.0, se introdujeron líneas adicionales entre las líneas de un cuadro de texto multilínea en postback si se usaba el elemento <xref:System.Web.Security.AntiXss.AntiXssEncoder?displayProperty=name>. En .NET Framework 4.5 no se incluyen estos saltos de línea adicionales, pero únicamente si la aplicación web tiene como destino .NET 4.5.|
|Sugerencia|Tenga en cuenta que las aplicaciones web de la versión 4.0 cuyo destino se haya cambiado a .NET 4.5 pueden tener cuadros de texto multilínea mejorados para dejar de introducir saltos de línea adicionales. Si esto no es deseable, la aplicación puede tener el comportamiento anterior cuando se ejecuta en .NET Framework 4.5 estableciendo como destino .NET Framework 4.0.|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Redestinación|

