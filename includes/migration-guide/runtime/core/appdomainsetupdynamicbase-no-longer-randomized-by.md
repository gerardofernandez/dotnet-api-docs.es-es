### <a name="appdomainsetupdynamicbase-is-no-longer-randomized-by-userandomizedstringhashalgorithm"></a>Ya no es aleatorio AppDomainSetup.DynamicBase por UseRandomizedStringHashAlgorithm

|   |   |
|---|---|
|Detalles|Antes de .NET Framework 4.6, el valor de <xref:System.AppDomainSetup.DynamicBase> ¿aleatorio entre dominios de aplicación, o entre los procesos, si UseRandomizedStringHashAlgorithm se habilitó en el archivo de configuración de la aplicación. A partir de la versión 4.6 de .NET Framework, <xref:System.AppDomainSetup.DynamicBase> devolverá un resultado estable entre diferentes instancias de una aplicación en ejecución y entre dominios de aplicación diferentes. Bases de datos dinámicos todavía serán diferentes para distintas aplicaciones; Este cambio solo quita el elemento de nomenclatura aleatorio para distintas instancias de la misma aplicación.|
|Sugerencia|Tenga en cuenta que permitir <code>UseRandomizedStringHashAlgorithm</code> no darán como resultado en <xref:System.AppDomainSetup.DynamicBase> se aleatorio. Si se necesita una base de aleatoria, se debe generar en el código de la aplicación, en lugar de hacerlo a través de esta API.|
|Ámbito|Borde|
|Versión|4.6|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.AppDomainSetup.DynamicBase?displayProperty=nameWithType></li></ul>|

