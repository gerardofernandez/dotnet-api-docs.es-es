### <a name="wf-serializes-expressionsliterallttgt-datetimes-differently-now-breaks-custom-xaml-parsers"></a>WF serializa Expressions.Literal&lt;T&gt; fechas y horas diferente ahora (interrumpe los analizadores XAML personalizados)

|   |   |
|---|---|
|Detalles|Asociado <xref:System.Windows.Markup.ValueSerializer> objeto convertirá un <xref:System.DateTime?displayProperty=name> o <xref:System.DateTimeOffset?displayProperty=name> objeto cuya en segundo lugar y <xref:System.DateTime.Millisecond?displayProperty=name> componentes son distintos de cero y (para un <xref:System.DateTime?displayProperty=name> valor) cuyo <xref:System.DateTime.Kind> propiedad no está especificada para el elemento de propiedad sintaxis en lugar de una cadena. Este cambio permite realizar un recorrido de ida y vuelta por los valores <xref:System.DateTime?displayProperty=name> y <xref:System.DateTimeOffset?displayProperty=name>. Los analizadores XAML personalizados que presuponen que la entrada XAML está en la sintaxis del atributo no funcionarán correctamente.|
|Sugerencia|Este cambio permite realizar un recorrido de ida y vuelta por los valores <xref:System.DateTime?displayProperty=name> y <xref:System.DateTimeOffset?displayProperty=name>. Los analizadores XAML personalizados que presuponen que la entrada XAML está en la sintaxis del atributo no funcionarán correctamente.|
|Ámbito|Borde|
|Versión|4.5|
|Tipo|Tiempo de ejecución|

