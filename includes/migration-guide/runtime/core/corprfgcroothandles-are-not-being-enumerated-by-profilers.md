### <a name="corprfgcroothandles-are-not-being-enumerated-by-profilers"></a>COR_PRF_GC_ROOT_HANDLEs no se está enumerando los generadores de perfiles

|   |   |
|---|---|
|Detalles|En el programa de v4.5.1 de .NET Framework, la API de generación de perfiles <code>RootReferences2()</code> incorrectamente nunca devuelve <code>COR_PRF_GC_ROOT_HANDLE</code> (se devuelven como <code>COR_PRF_GC_ROOT_OTHER</code> en su lugar). Este problema se corrigió a partir de .NET Framework 4.6.|
|Sugerencia|Este problema se ha solucionado en .NET Framework 4.6 y puede solucionarse al actualizar a esa versión de .NET Framework.|
|Ámbito|Secundaria|
|Versión|4.5.1|
|Tipo|Tiempo de ejecución|

