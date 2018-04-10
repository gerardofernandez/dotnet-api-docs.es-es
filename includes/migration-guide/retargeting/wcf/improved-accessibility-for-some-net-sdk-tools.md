### <a name="improved-accessibility-for-some-net-sdk-tools"></a>Mejorar la accesibilidad para algunas herramientas de SDK para .NET

|   |   |
|---|---|
|Detalles|En .NET Framework SDK 4.7.1, se han mejorado las herramientas de svcconfigedit.exe y svctraceviewer.exe si corrige problemas de accesibilidad variadas. La mayoría de estas eran pequeños detalles como un nombre no está definido o determinados patrones de automatización de la interfaz de usuario no se implementa correctamente. Mientras que muchos usuarios no sería compatible con estos valores incorrectos, los clientes que usan las tecnologías de asistencia como lectores de pantalla encontrará estas herramientas SDK sea más accesible. De hecho, estas correcciones cambiar algunos comportamientos anteriores, como el pedido de foco de teclado. Para obtener todas las correcciones de la accesibilidad en estas herramientas, puede lo siguiente en el archivo app.config:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Ámbito|Borde|
|Versión|4.7.1|
|Tipo|Redestinación|

