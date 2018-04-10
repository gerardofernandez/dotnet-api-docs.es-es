### <a name="remove-ssl3-from-the-wcf-transportdefaults"></a>Quite Ssl3 el TransportDefaults WCF

|   |   |
|---|---|
|Detalles|Al usar NetTcp con seguridad de transporte y un tipo de credencial de certificado, el protocolo SSL 3 ya no es el protocolo predeterminado para negociar una conexión segura. En la mayoría de los casos no debe haber ningún impacto en las aplicaciones existentes como TLS 1.0 siempre se ha incluido en la lista de protocolos NetTcp. Todos los clientes deberían poder negociar una conexión usando como mínimo TLS1.0.|
|Sugerencia|Si es necesario Ssl3, utilice uno de los siguientes mecanismos de configuración para agregar Ssl3 a la lista de protocolos negociados.<ul><li><xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement.SslProtocols></li><li><xref:System.ServiceModel.TcpTransportSecurity.SslProtocols></li><li>[<](~/docs/framework/configure-apps/file-schema/wcf/transport-of-nettcpbinding.md)</li><li>[&lt;sslStreamSecurity&gt; sección de &lt;customBinding&gt;] ~ / docs/framework/configure-apps/file-schema/wcf/sslstreamsecurity.md)</li></ul>|
|Ámbito|Borde|
|Versión|4.6.2|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement.SslProtocols?displayProperty=nameWithType></li><li><xref:System.ServiceModel.TcpTransportSecurity.SslProtocols?displayProperty=nameWithType></li></ul>|

