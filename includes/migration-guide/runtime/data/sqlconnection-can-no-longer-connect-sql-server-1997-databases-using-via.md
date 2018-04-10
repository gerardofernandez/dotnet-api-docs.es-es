### <a name="sqlconnection-can-no-longer-connect-to-sql-server-1997-or-databases-using-the-via-adapter"></a>SqlConnection ya no puede conectarse a SQL Server 1997 o bases de datos mediante el adaptador VIA

|   |   |
|---|---|
|Detalles|Las conexiones a bases de datos de SQL Server mediante la [protocolo de adaptador de interfaz Virtual (VIA)](https://technet.microsoft.com/library/ms191229%28v=sql.105%29.aspx) ya no se admiten. El protocolo utilizado para conectarse a una base de datos de SQL Server está visible en la cadena de conexión. Una conexión de VIA contendrá a través de:&lt;servername&gt;. Si esta aplicación se conecta a SQL a través de un protocolo distinto de VIA (tcp: o np: por ejemplo), a continuación, no se encuentre ningún cambio importante. Además, ya no se admiten las conexiones a SQL Server 7 (1997).|
|Sugerencia|El protocolo VIA está en desuso, por lo que se debe usar un protocolo alternativo para conectarse a bases de datos SQL. El protocolo más utilizado es TCP/IP. Encontrará instrucciones para habilitar el protocolo TCP/IP [aquí](https://msdn.microsoft.com/library/bb909712.aspx). Si solo se tiene acceso desde la base de datos dentro de una intranet, el protocolo de canalizaciones compartida puede proporcionar un mejor rendimiento si la red es lenta.|
|Ámbito|Borde|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String,System.Data.SqlClient.SqlCredential)?displayProperty=nameWithType></li></ul>|

