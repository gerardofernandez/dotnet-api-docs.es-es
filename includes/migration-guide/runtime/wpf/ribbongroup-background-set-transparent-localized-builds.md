### <a name="ribbongroup-background-is-set-to-transparent-in-localized-builds"></a>Fondo de RibbonGroup se establece en transparente en las compilaciones localizadas

|   |   |
|---|---|
|Detalles|<xref:System.Windows.Controls.Ribbon.RibbonGroup?displayProperty=name> siempre se pinta el fondo en las compilaciones localizadas con pincel transparente, lo que produce una mala experiencia de interfaz de usuario. Esto se fija en .NET 4,7 corrección WPF mediante la actualización de los recursos localizados para <xref:System.Windows.Controls.Ribbon.RibbonGroup?displayProperty=name>, a su vez, lo que garantiza que el pincel correcto está seleccionado.|
|Sugerencia|Actualización a .NET 4.7|
|Ámbito|Borde|
|Versión|4.6.2|
|Tipo|Tiempo de ejecución|

