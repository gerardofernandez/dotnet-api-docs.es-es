### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>NullReferenceException en código de ImageSourceConverter.ConvertFrom de control de excepciones

|   |   |
|---|---|
|Detalles|Un error en el código de control de excepciones <xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)> provocó incorrecta <xref:System.NullReferenceException?displayProperty=name> que se produzca en lugar de la excepción deseada (por ejemplo, <xref:System.IO.DirectoryNotFoundException?displayProperty=name>, <xref:System.IO.FileNotFoundException?displayProperty=name>), este cambio corrige el error para que el método ahora produce la excepción correcta. Forma predeterminada todas las aplicaciones orientadas a .NET Framework 4.6.2 y a continuación continuará produzca <xref:System.NullReferenceException?displayProperty=name> para compatibilidad, los desarrolladores se centran 4.7 de .NET Framework y versiones posteriores debería ver el derecho exceptions.// reemplazar el espacio con una 'x' Si es aplicable|
|Sugerencia|Los desarrolladores que deseen volver a obtener <xref:System.NullReferenceException?displayProperty=name> cuando como destino .NET Framework 4.7 puede agregar/merge lo siguiente al archivo de App.config de su aplicación:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Ámbito|Borde|
|Versión|4.7|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

