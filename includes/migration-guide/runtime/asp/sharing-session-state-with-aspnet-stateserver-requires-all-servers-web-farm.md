### <a name="sharing-session-state-with-aspnet-stateserver-requires-all-servers-in-the-web-farm-to-use-the-same-net-framework-version"></a>Compartir el estado de sesión con Asp.Net StateServer requiere que todos los servidores de la granja de servidores web para usar la misma versión de .NET Framework

|   |   |
|---|---|
|Detalles|Al habilitar <xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=name> de estado de sesión, todos los servidores en la granja de servidores web determinado deben usar la misma versión de .NET Framework para el estado de compartir correctamente.|
|Sugerencia|Asegúrese de actualizar las versiones de .NET Framework en los servidores web que compartan el estado al mismo tiempo.|
|Ámbito|Borde|
|Versión|4.5|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=nameWithType></li></ul>|

