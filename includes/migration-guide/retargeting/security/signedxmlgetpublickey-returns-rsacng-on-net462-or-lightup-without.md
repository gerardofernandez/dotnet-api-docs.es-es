### <a name="signedxmlgetpublickey-returns-rsacng-on-net462-or-lightup-without-retargeting-change"></a>SignedXml.GetPublicKey devuelve RSACng en net462 (o explicar) sin cambios de redestinación

|   |   |
|---|---|
|Detalles|A partir de .NET Framework 4.6.2, el tipo concreto del objeto devuelto por la <xref:System.Security.Cryptography.Xml.SignedXml.GetPublicKey%2A?displayProperty=nameWithType> método cambiado (sin una anomalía) de una implementación de CryptoServiceProvider a una implementación de Cng. Esto es porque ha cambiado la implementación de uso <code>certificate.PublicKey.Key</code> al uso interno <code>certificate.GetAnyPublicKey</code> que reenvía al <xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey%2A?displayProperty=nameWithType>.|
|Sugerencia|A partir de aplicaciones que se ejecutan en .NET Framework 4.7.1, puede usar la implementación de CryptoServiceProvider usa de forma predeterminada en .NET Framework 4.6.1 y versiones anteriores mediante la adición de la siguiente configuración se cambia a la [en tiempo de ejecución](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)sección de su archivo de configuración de aplicación:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.SignedXmlUseLegacyCertificatePrivateKey=true&quot; /&gt;&#13;&#10;</code></pre>|
|Ámbito|Borde|
|Versión|4.6.2|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.Security.Cryptography.Xml.SignedXml.CheckSignatureReturningKey(System.Security.Cryptography.AsymmetricAlgorithm@)?displayProperty=nameWithType></li></ul>|

