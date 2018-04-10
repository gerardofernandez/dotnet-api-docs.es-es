### <a name="rsacngverifyhash-now-returns-false-for-any-verification-failure"></a>RSACng.VerifyHash ahora devuelve False para los errores de comprobación

|   |   |
|---|---|
|Detalles|A partir de .NET Framework 4.6.2, este método devuelve <strong>False</strong> si la firma propiamente dicha se formato incorrecto. Ahora devuelve false para los errores de comprobación. En .NET Framework 4.6 y 4.6.1, el método produce una <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> si la firma propiamente dicha se formato incorrecto.|
|Sugerencia|Cualquier código cuya ejecución depende de control de la <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> en su lugar, debe ejecutar si se produce un error de validación y el método devuelve <strong>False</strong>.|
|Ámbito|Secundaria|
|Versión|4.6.2|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Security.Cryptography.RSACng.VerifyHash(System.Byte[],System.Byte[],System.Security.Cryptography.HashAlgorithmName,System.Security.Cryptography.RSASignaturePadding)?displayProperty=nameWithType></li></ul>|

