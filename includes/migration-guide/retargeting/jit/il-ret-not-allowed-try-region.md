### <a name="il-ret-not-allowed-in-a-try-region"></a>IL ret no se permite en una región de try

|   |   |
|---|---|
|Detalles|Al contrario que el compilador de just-in-time JIT64, RyuJIT (que se usa en .NET 4.6) no permite un IL ret instrucción en una región de try. Devolver desde una región try no permite la especificación de ECMA-335 y ningún compilador administrado conocido genera tal IL. Sin embargo, el compilador JIT64 ejecutará dicho IL si se genera mediante la emisión de reflexión.|
|Sugerencia|Si una aplicación está generando código IL que incluye un código de operación ret en una región de try, la aplicación puede tener como destino .NET 4.5 para usar el antiguo JIT y evite este salto. Como alternativa, puede actualizarse el IL generado para devolver después de la región de try.|
|Ámbito|Borde|
|Versión|4.6|
|Tipo|Redestinación|

