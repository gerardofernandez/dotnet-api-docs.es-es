### <a name="targetframeworkname-for-default-app-domain-no-longer-defaults-to-null-if-not-set"></a>TargetFrameworkName de dominio de aplicación predeterminado ya no tiene como valor predeterminado para null si no está establecido

|   |   |
|---|---|
|Detalles|El <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> era anteriormente null en el dominio de aplicación predeterminado, a menos que se estableció explícitamente. A partir de la versión 4.6, la <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> propiedad para el dominio de aplicación predeterminado tenga un valor predeterminado derivado TargetFrameworkAttribute (si la hay). Dominios de aplicación no predeterminado continuarán heredan sus <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> desde el dominio de aplicación predeterminado (que no serán null de la versión 4.6) a menos que se invalide explícitamente.|
|Sugerencia|El código debería actualizarse para no depender de que <xref:System.AppDomainSetup.TargetFrameworkName> establezca un valor nulo como valor predeterminado. Si es necesario que esta propiedad continúe evaluándose como un valor nulo, puede establecerse en dicho valor de forma explícita.|
|Ámbito|Borde|
|Versión|4.6|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=nameWithType></li></ul>|

