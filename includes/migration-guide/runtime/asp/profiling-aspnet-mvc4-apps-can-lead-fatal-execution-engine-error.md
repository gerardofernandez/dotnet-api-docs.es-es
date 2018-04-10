### <a name="profiling-aspnet-mvc4-apps-can-lead-to-fatal-execution-engine-error"></a>Generar perfiles de aplicaciones de ASP.Net MVC4 pueden provocar el Error irrecuperable del motor de ejecución

|   |   |
|---|---|
|Detalles|Los generadores de perfiles mediante ensamblados NGEN /Profile pueden bloquearse para aplicaciones de ASP.NET MVC4 durante el inicio con un 'excepción de motor de ejecución de grave'|
|Sugerencia|Este problema se corregirá en .NET Framework 4.5.2. Como alternativa, el generador de perfiles puede evitar este problema mediante la especificación de <code>COR_PRF_DISABLE_ALL_NGEN_IMAGES</code> en su máscara de eventos.|
|Ámbito|Borde|
|Versión|4.5|
|Tipo|Tiempo de ejecución|

