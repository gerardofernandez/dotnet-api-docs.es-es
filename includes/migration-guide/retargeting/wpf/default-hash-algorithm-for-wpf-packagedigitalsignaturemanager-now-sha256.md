### <a name="the-default-hash-algorithm-for-wpf-packagedigitalsignaturemanager-is-now-sha256"></a>El algoritmo hash predeterminado para WPF entre ahora es SHA256

|   |   |
|---|---|
|Detalles|El <code>System.IO.Packaging.PackageDigitalSignatureManager</code> proporciona funcionalidad para las firmas digitales en relación con paquetes WPF.  4.7 de .NET Framework y versiones anteriores, el algoritmo predeterminado (<xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType>) utilizado para firmar las partes de un paquete era SHA1.  Por motivos de seguridad recientes con SHA1, este valor predeterminado se ha cambiado a SHA256 a partir de .NET Framework 4.7.1.  Este cambio afecta a todas las firmas de los paquetes, incluidos los documentos XPS.|
|Sugerencia|Un desarrollador que desea usar este cambio al especificar una versión de framework debajo .NET 4.7.1 o un desarrollador que requiera la funcionalidad anterior al tienen como destino .NET 4.7.1 o mayor puede establece la siguiente marca de AppContext correctamente.  Dará como resultado un valor true en SHA1 se usa como el algoritmo predeterminado; False, se producirá en SHA256.<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.UseSha1AsDefaultHashAlgorithmForDigitalSignatures=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Ámbito|Borde|
|Versión|4.7.1|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType></li></ul>|

