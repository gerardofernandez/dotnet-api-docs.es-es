### <a name="xsd-schema-validation-now-correctly-detects-violations-of-unique-constraints-if-compound-keys-are-used-and-one-key-is-empty"></a>La validación del esquema XSD ahora detecta correctamente las infracciones de restricciones unique si se usan las claves compuestas y una clave está vacía

|   |   |
|---|---|
|Detalles|Las versiones de .NET Framework anteriores a la 4.6 presentaban un error que hacía que la validación de XSD no detectara restricciones únicas en claves compuestas si alguna de las claves estaba vacía. Este problema se corrigió en .NET Framework 4.6. De este modo, se conseguirá una mayor corrección en la validación, pero también podría hacer que cierto XML no valide lo que antes sí validaría.|
|Sugerencia|Si es necesaria la validación más flexible de .NET Framework 4.0, la aplicación de validación puede tener como destino versión 4.5 (o anterior) de .NET Framework. No obstante, al cambiar el destino a .NET Framework 4.6, debería revisarse el código para asegurarse de que no se espere la validación de claves compuestas duplicadas (como se indica en la descripción de este problema).|
|Ámbito|Borde|
|Versión|4.6|
|Tipo|Redestinación|

