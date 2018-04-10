### <a name="sqlbulkcopy-uses-destination-column-encoding-for-strings"></a>SqlBulkCopy usa la codificación de columna de destino para las cadenas

|   |   |
|---|---|
|Detalles|Al insertar datos en una columna, <xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> utiliza la codificación de la columna de destino en lugar de la codificación predeterminada para los tipos <code>VARCHAR</code> y <code>CHAR</code>. Este cambio elimina la posibilidad de que se produzcan daños en los datos al usar la codificación predeterminada cuando la columna de destino no utiliza la codificación predeterminada. En raras ocasiones, una aplicación existente podría producir una excepción SqlException si el cambio de codificación produce datos que son demasiado grandes para caber en la columna de destino.|
|Sugerencia|Espera que <xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> ya no se dañará datos debido a diferencias de codificación. Si se copian cadenas cerca del límite de tamaño de la columna de destino, puede ser necesario o codificar previamente copiar los datos (para comprobar que los datos quepan en la columna de destino) o catch <xref:System.Data.SqlClient.SqlException?displayProperty=name>s.|
|Ámbito|Borde|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlBulkCopy.%23ctor(System.Data.SqlClient.SqlConnection)?displayProperty=nameWithType></li></ul>|

