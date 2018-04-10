### <a name="winforms-checkforoverflowunderflow-property-is-now-true-for-systemdrawing"></a>Ahora es true para System.Drawing CheckForOverflowUnderflow (propiedad) del WinForm

|   |   |
|---|---|
|Detalles|La propiedad CheckForOverflowUnderflow para el ensamblado System.Drawing.dll está establecida en true.|
|Sugerencia|Anteriormente, cuando se producían desbordamientos, el resultado se truncaba de manera silenciosa. Ahora se inicia una excepción <xref:System.OverflowException?displayProperty=name>.|
|Ámbito|Borde|
|Versión|4.5|
|Tipo|Tiempo de ejecución|

