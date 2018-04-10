### <a name="calls-to-systemwindowsinputpencontextdisable-on-touch-enabled-systems-may-throw-an-argumentexception"></a>Las llamadas a System.Windows.Input.PenContext.Disable en sistemas táctil pueden producir una excepción ArgumentException

|   |   |
|---|---|
|Detalles|En algunas circunstancias, las llamadas a interno <strong>System.Windows.Intput.PenContext.Disable</strong> método en sistemas táctil puede producir una no controlada <code>T:System.ArgumentException</code> debido a la reentrada.|
|Sugerencia|Este problema se ha corregido en el 4.7 de .NET Framework. Para evitar la excepción, actualice a una versión de .NET Framework a partir de la 4.7 de .NET Framework.|
|Ámbito|Borde|
|Versión|4.6.1|
|Tipo|Redestinación|

