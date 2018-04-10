### <a name="managed-browser-hosting-controls-from-the-net-framework-11-and-20-are-blocked"></a>Controles de hospedaje de explorador administrado de .NET Framework 1.1 y 2.0 están bloqueados

|   |   |
|---|---|
|Detalles|El hospedaje de estos controles está bloqueado en Internet Explorer.|
|Sugerencia|Internet Explorer no podrá iniciar una aplicación que use controles de hospedaje de explorador administrados. Se puede restaurar el comportamiento anterior estableciendo el valor EnableIEHosting de la subclave del registro <code>HKLM/SOFTWARE/MICROSOFT/.NETFramework</code> a <code>1</code> para x86 sistemas y para los procesos de 32 bits en x64 sistemas y estableciendo el <code>EnableIEHosting</code> valor de la subclave del registro <code>HKLM/SOFTWARE/Wow6432Node/Microsoft/.NETFramework</code>a <code>1</code> para procesos de 64 bits en x64 sistemas.|
|Ámbito|Secundaria|
|Versión|4.5|
|Tipo|Tiempo de ejecución|

