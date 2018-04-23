### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>Excepción NullReferenceException en el código de control de excepciones de ImageSourceConverter.ConvertFrom

|   |   |
|---|---|
|Detalles|Un error en el código de control de excepciones de <xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)> provocaba que se iniciara una excepción <xref:System.NullReferenceException?displayProperty=name> incorrecta en lugar de la excepción prevista (por ejemplo, <xref:System.IO.DirectoryNotFoundException?displayProperty=name>, <xref:System.IO.FileNotFoundException?displayProperty=name>), este cambio corrige el error para que el método ahora inicie la excepción correcta. De forma predeterminada, todas las aplicaciones destinadas a .NET Framework 4.6.2 y versiones posteriores seguirán iniciando <xref:System.NullReferenceException?displayProperty=name> con fines de compatibilidad, los desarrolladores que elijan .NET Framework 4.7 y versiones posteriores como destino deberían ver las excepciones correctas.// Si procede, reemplace el espacio con una "x".|
|Sugerencia|Los desarrolladores que quieran volver a obtener <xref:System.NullReferenceException?displayProperty=name> cuando el destino sea .NET Framework 4.7, pueden agregar o combinar lo siguiente en el archivo App.config de la aplicación:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Ámbito|Borde|
|Versión|4.7|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

