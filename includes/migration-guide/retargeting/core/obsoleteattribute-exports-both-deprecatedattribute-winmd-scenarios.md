### <a name="obsoleteattribute-exports-as-both-obsoleteattribute-and-deprecatedattribute-in-winmd-scenarios"></a>ObsoleteAttribute exporta como ObsoleteAttribute y DeprecatedAttribute en escenarios de WinMD

|   |   |
|---|---|
|Detalles|Cuando se crea una biblioteca de metadatos de Windows (archivo .winmd), el <xref:System.ObsoleteAttribute?displayProperty=name> atributo se exporta como <xref:System.ObsoleteAttribute?displayProperty=name> y [Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute).|
|Sugerencia|Volver a compilar el código fuente existente que usa el <xref:System.ObsoleteAttribute?displayProperty=name> atributo puede generar advertencias al utilizar ese código desde C++ / CX o JavaScript.We no se recomienda aplicar <xref:System.ObsoleteAttribute?displayProperty=name> y [ Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute) al código en los ensamblados administrados; se podrían producir advertencias de compilación.|
|Ámbito|Borde|
|Versión|4.5.1|
|Tipo|Redestinación|

