### <a name="attempting-a-tcpip-connection-to-a-sql-server-database-that-resolves-to-localhost-fails"></a>Intento de conexión TCP/IP con una base de datos de SQL Server que se resuelve como `localhost` se produce un error

|   |   |
|---|---|
|Detalles|En .NET Framework 4.6 y 4.6.1, intentar una conexión TCP/IP para una base de datos de SQL Server que se resuelve en <code>localhost</code> genera el error &quot;produjo un error relacionado con la red o específico de la instancia al establecer una conexión con SQL Server. No se encontró el servidor o éste no estaba accesible. Compruebe que el nombre de la instancia es correcto y que SQL Server está configurado para admitir conexiones remotas. (proveedor: Interfaces de red SQL, error: 26 - Error Buscar servidor/instancia especificado)&quot;|
|Sugerencia|Este problema se ha solucionado y restaura el comportamiento anterior de .NET Framework 4.6.2. Para conectarse a un databsae de SQL Server que se resuelve como <code>localhost</code>, actualice a .NET Framework 4.6.2.|
|Ámbito|Secundaria|
|Versión|4.6|
|Tipo|Tiempo de ejecución|

