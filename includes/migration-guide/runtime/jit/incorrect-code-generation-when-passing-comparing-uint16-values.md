### <a name="incorrect-code-generation-when-passing-and-comparing-uint16-values"></a>Generación de código incorrecto al pasar y comparar valores UInt16.

|   |   |
|---|---|
|Detalles|Debido a los cambios introducidos en la 4.7 de .NET Framework, en algunos casos el código generado por el compilador JIT en aplicaciones que se ejecutan en el 4.7 de .NET Framework incorrectamente compara dos <code>T:System.UInt16</code> valores. Para obtener más información, consulte [problema #11508: codegen incorrecto silencioso al pasar y comparar ushort args](https://github.com/dotnet/coreclr/issues/11508) en GitHub.com.|
|Sugerencia|Si se producen problemas en la comparación de valores de 16 bits sin signo en la 4.7 de .NET Framework, actualizar a .NET Framework 4.7.1.|
|Ámbito|Borde|
|Versión|4.7|
|Tipo|Tiempo de ejecución|

