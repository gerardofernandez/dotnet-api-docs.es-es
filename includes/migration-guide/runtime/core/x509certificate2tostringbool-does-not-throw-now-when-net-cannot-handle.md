### <a name="x509certificate2tostringbool-does-not-throw-now-when-net-cannot-handle-the-certificate"></a>X509Certificate2.ToString(bool) no produce una excepción cuando .NET no se controlan ahora el certificado

|   |   |
|---|---|
|Detalles|Anteriormente, este método se producirá si <code>true</code> se pasó para el parámetro verbose y no hay certificados instalados que no eran compatibles con .NET Framework. Ahora, el método se realizará correctamente y devuelven una cadena válida que omita las partes inaccesibles del certificado.|
|Sugerencia|Cualquier código en función de <xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)> deben actualizarse para esperar que la cadena devuelta puede excluir algunos datos de certificado (por ejemplo, la clave pública, clave privada y extensiones) en algunos casos donde la API habría inició previamente.|
|Ámbito|Borde|
|Versión|4.6|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)?displayProperty=nameWithType></li></ul>|

