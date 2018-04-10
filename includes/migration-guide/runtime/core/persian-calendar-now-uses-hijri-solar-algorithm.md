### <a name="persian-calendar-now-uses-the-hijri-solar-algorithm"></a>Calendario persa ahora usa el algoritmo Hijri solar

|   |   |
|---|---|
|Detalles|A partir de la versión 4.6 de .NET Framework, el <xref:System.Globalization.PersianCalendar?displayProperty=name> clase utiliza el algoritmo Hijri solar. Convertir las fechas entre el <xref:System.Globalization.PersianCalendar?displayProperty=name> y otros calendarios pueden producir un resultado ligeramente diferente a partir la versión 4.6 de .NET Framework para las fechas anteriores a 1800 o posteriores a 2023 (gregoriano). Además, <xref:System.Globalization.PersianCalendar.MinSupportedDateTime> es ahora <code>March 22, 0622 instead of March 21, 0622</code>.|
|Sugerencia|Tenga en cuenta que algunas fechas tempranas o tardías pueden ser ligeramente diferentes al utilizar PersianCalendar en .NET Framework 4.6. Además, al serializar fechas entre procesos que puedan ejecutarse en diferentes versiones de .NET Framework, no las guarde como cadenas de fecha de PersianCalendar (ya que estos valores pueden ser diferentes).|
|Ámbito|Secundaria|
|Versión|4.6|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Globalization.PersianCalendar?displayProperty=nameWithType></li></ul>|

