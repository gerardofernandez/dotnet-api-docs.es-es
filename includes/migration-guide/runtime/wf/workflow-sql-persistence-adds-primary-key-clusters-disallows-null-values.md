### <a name="workflow-sql-persistence-adds-primary-key-clusters-and-disallows-null-values-in-some-columns"></a>Persistencia de SQL de flujo de trabajo agrega los clústeres de clave principal y no permite valores null en algunas columnas

|   |   |
|---|---|
|Detalles|A partir de la 4.7 de .NET Framework, las tablas creadas para el almacén de instancia de flujo de trabajo de SQL (SWIS) por el script SqlWorkflowInstanceStoreSchema.sql usan claves principales en clúster. Por este motivo, no se admiten las identidades <code>null</code> valores. La operación de SWIS no se ve afectada por este cambio. Las actualizaciones se realizaron para admitir la replicación transaccional de SQL Server.|
|Sugerencia|El archivo SQL SqlWorkflowInstanceStoreSchemaUpgrade.sql debe aplicarse a las instalaciones existentes con el fin de experimentar este cambio. Nuevas instalaciones de la base de datos tendrá automáticamente el cambio.|
|Ámbito|Borde|
|Versión|4.7|
|Tipo|Tiempo de ejecución|

