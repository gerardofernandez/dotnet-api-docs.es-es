### <a name="x509certificateclaimsetfindclaims-considers-all-claimtypes"></a>X509CertificateClaimSet.FindClaims considera que todas sus claimTypes

|   |   |
|---|---|
|Detalles|En aplicaciones que tienen como destino .NET Framework 4.6.1, si un conjunto de notificaciones se inicia desde un certificado que tenga varias entradas DNS en su campo SAN, de X509 la <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> método intenta hacer coincidir el argumento claimType con todas las entradas DNS. Para las aplicaciones que tienen como destino versiones anteriores de .NET Framework, el <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> método intenta hacer coincidir el argumento claimType solo con la última entrada DNS.|
|Sugerencia|Este cambio solo afecta a las aplicaciones que tengan como destino .NET Framework 4.6.1. Este cambio puede deshabilitarse (o habilitarse si se establece como destino una versión anterior a la 4.6.1) con el modificador de compatibilidad [DisableMultipleDNSEntries](~/docs/framework/migration-guide/mitigation-x509certificateclaimset-findclaims-method.md#mitigation).|
|Ámbito|Secundaria|
|Versión|4.6.1|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=nameWithType></li></ul>|

