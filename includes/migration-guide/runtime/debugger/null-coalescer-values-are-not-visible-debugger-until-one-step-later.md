### <a name="null-coalescer-values-are-not-visible-in-debugger-until-one-step-later"></a>Valores NULL fusionador no están visibles en el depurador hasta un paso más adelante

|   |   |
|---|---|
|Detalles|Un error en .NET Framework 4.5 hace que los valores establecidos mediante una operación de fusión null no esté visible en el depurador inmediatamente después de la operación de asignación se ejecuta cuando se ejecuta en la versión de 64 bits de Framework.|
|Sugerencia|Ejecución paso a paso una vez adicional en el depurador hará que el local/valor del campo se actualicen correctamente. Además, este problema se ha solucionado en la versión 4.6 de .NET Framework; actualizar a esa versión de Framework, debe resolver el problema.|
|Ámbito|Borde|
|Versión|4.5|
|Tipo|Tiempo de ejecución|

