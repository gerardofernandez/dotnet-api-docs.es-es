### <a name="ipad-should-not-be-used-in-custom-capabilities-file-because-it-is-now-a-browser-capability"></a>IPad no debe usarse en el archivo de las capacidades personalizadas como ahora es una funcionalidad de explorador

|   |   |
|---|---|
|Detalles|A partir de .NET 4.5, iPad es un identificador en el archivo de funciones de explorador ASP.NET de forma predeterminada, por lo que no debe usarse en un archivo de las capacidades personalizadas|
|Sugerencia|Si se requieren capacidades específicas de iPad, es necesario modificar el comportamiento de iPad estableciendo capacidades en la puerta de enlace predefinido refID &quot;IPad&quot; en lugar de mediante la generación de un nuevo &quot;IPad&quot; Id. de agente de usuario búsqueda de coincidencias.|
|Ámbito|Borde|
|Versión|4.5|
|Tipo|Tiempo de ejecución|

