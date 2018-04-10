### <a name="different-exception-handling-for-objectcontextcreatedatabase-and-dbproviderservicescreatedatabase-methods"></a>Otro control de excepciones de los métodos ObjectContext.CreateDatabase y DbProviderServices.CreateDatabase

|   |   |
|---|---|
|Detalles|A partir de .NET Framework 4.5, si se produce un error de creación de base de datos, los métodos <code>CreateDatabase</code> tratarán de eliminar la base de datos vacía. Si la operación se realiza correctamente, se propagará el elemento <xref:System.Data.SqlClient.SqlException?displayProperty=name> original (en lugar del elemento <xref:System.InvalidOperationException?displayProperty=name>, que ya se iniciaba siempre en .NET Framework 4.0).|
|Sugerencia|Cuando detecta un <xref:System.InvalidOperationException?displayProperty=name> al ejecutar <xref:System.Data.Objects.ObjectContext.CreateDatabase> o <xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)>, SQLExceptions ahora también se debe detectar.|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)?displayProperty=nameWithType></li></ul>|

