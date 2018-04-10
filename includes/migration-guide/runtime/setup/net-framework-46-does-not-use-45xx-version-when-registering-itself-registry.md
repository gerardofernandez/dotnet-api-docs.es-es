### <a name="the-net-framework-46-does-not-use-a-45xx-version-when-registering-itself-in-the-registry"></a>.NET Framework 4.6 no utiliza una versión de 4.5.x.x al registrarse a sí mismo en el registro

|   |   |
|---|---|
|Detalles|Tal y como se podría esperar que la clave de versión se establece en el registro (en <code>HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\NET Framework Setup\NDP\v4\Full</code>) para .NET Framework 4.6 comienza con '4.6', no '4.5'. Las aplicaciones que dependen de estas claves del registro para saber qué versiones de .NET Framework están instaladas en un equipo deben actualizarse para entender que 4.6 es una nueva versión posibles, y uno que sea compatible con 4.5 anterior libera.|
|Sugerencia|Las aplicaciones de actualización sondeo para un equipo con .NET Framework 4.5 se instalan buscando 4.5 claves del registro Aceptar también 4.6.|
|Ámbito|Borde|
|Versión|4.6|
|Tipo|Tiempo de ejecución|

