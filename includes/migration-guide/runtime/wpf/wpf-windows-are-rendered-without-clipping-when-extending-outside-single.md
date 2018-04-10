### <a name="wpf-windows-are-rendered-without-clipping-when-extending-outside-a-single-monitor"></a>Las ventanas de WPF se representan sin recortes al extender fuera de un solo monitor

|   |   |
|---|---|
|Detalles|Durante la ejecución en Windows 8 y versiones posteriores de .NET Framework 4.6, toda la ventana se representa sin recortes al extenderse más allá de la pantalla solo en un escenario de varios monitor. Esto es diferente de versiones anteriores de .NET Framework que se recorta las ventanas de WPF que extender más allá de una sola pantalla.|
|Sugerencia|Este comportamiento (si hay que recortar o no) se pueden establecer explícitamente mediante la <code>&lt;EnableMultiMonitorDisplayClipping&gt;</code> elemento <code>&lt;appSettings&gt;</code> en el archivo de configuración de la aplicación, o estableciendo la <code>EnableMultiMonitorDisplayClipping</code> propiedad durante el inicio de la aplicación.|
|Ámbito|Secundaria|
|Versión|4.6|
|Tipo|Tiempo de ejecución|

