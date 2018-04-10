### <a name="etw-event-names-cannot-differ-only-by-a-start-or-stop-suffix"></a>Los nombres de eventos ETW no pueden diferenciarse solo por un sufijo "Start" o "Stop"

|   |   |
|---|---|
|Detalles|En .NET Framework 4.6 y 4.6.1, el runtime produce una <xref:System.ArgumentException> cuando dos nombres de evento de seguimiento de eventos para Windows (ETW) solo se diferencian entre un &quot;iniciar&quot; o &quot;detener&quot; sufijo (como cuando un evento se denomina <code>LogUser</code>y otro denominado <code>LogUserStart</code>). En este caso, el entorno en tiempo de ejecución no puede crear el origen de eventos, que no puede emitir ningún registro.|
|Sugerencia|Para evitar la excepción, asegúrese de que no hay nombres de dos eventos solo se diferencian entre un &quot;iniciar&quot; o &quot;detener&quot; sufijo. Se ha eliminado este requisito a partir de .NET Framework 4.6.2; el tiempo de ejecución puede eliminar la ambigüedad de los nombres de evento que se diferencien solo por la &quot;iniciar&quot; y &quot;detener&quot; sufijo.|
|Ámbito|Borde|
|Versión|4.6|
|Tipo|Redestinación|

