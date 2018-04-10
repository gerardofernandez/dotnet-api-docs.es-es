### <a name="foreach-iterator-variable-is-now-scoped-within-the-iteration-so-closure-capturing-semantics-are-different-in-c5"></a>Variable de iteración foreach ahora dentro del ámbito de la iteración, por lo que es diferente (en C# 5) captura semántica de cierre

|   |   |
|---|---|
|Detalles|A partir de C# 5 (Visual Studio 2012), <code>foreach</code> variables de iteración se aplican a la iteración. Esto puede causar saltos si código previamente se dependiendo de las variables que no se incluirá en el <code>foreach</code>del cierre. El síntoma de este cambio es que una variable de iteración que se pasa a un delegado se trata como el valor tiene en el momento que el delegado se crea, en lugar del valor que tiene en el momento en que se invoca el delegado.|
|Sugerencia|Lo ideal sería actualizar el código para que espere el nuevo comportamiento del compilador. Si es necesario usar la semántica anterior, es posible reemplazar la variable de iterador por una variable independiente colocada de forma explícita fuera del ámbito del bucle.|
|Ámbito|Major|
|Versión|4.5|
|Tipo|Redestinación|

