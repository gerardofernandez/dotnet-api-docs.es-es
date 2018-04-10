### <a name="clickonce-supports-sha-256-on-40-targeted-apps"></a>ClickOnce admite SHA-256 en aplicaciones dirigidas a la 4.0

|   |   |
|---|---|
|Detalles|Anteriormente, una aplicación ClickOnce con un certificado firmado con SHA-256 requeriría .NET 4.5 o posterior esté presente, incluso si la aplicación de destino 4.0. Ahora, pueden ejecutar aplicaciones ClickOnce dirigidas al 4.0 en 4.0, incluso si está firmado con SHA-256.|
|Sugerencia|Este cambio elimina esa dependencia y permite que los certificados de SHA-256 firmar las aplicaciones ClickOnce que tienen como destino .NET Framework 4 y versiones anteriores.|
|Ámbito|Secundaria|
|Versión|4.6|
|Tipo|Redestinación|

