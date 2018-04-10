### <a name="chained-popups-with-staysopenfalse"></a>Encadenar los menús emergentes con StaysOpen = False

|   |   |
|---|---|
|Detalles|Un menú emergente con StaysOpen = False se supone que se cerrará al hacer clic fuera de la ventana emergente. Cuando se encadenan dos o más tales emergentes (es decir, uno que contiene otra), se han producido muchos problemas, incluidos:<ul><li>Abra dos niveles, haga clic en fuera P2 pero dentro de P1.  No ocurre nada.</li><li>Abra dos niveles, haga clic en P1 exterior.  Cierre las ventanas emergentes.</li><li>Abrir y cerrar los dos niveles.  A continuación, intente volver a abrir P2.  No ocurre nada.</li><li>Pruebe a abrir tres niveles.  No puedes.  (No sucede nada o cerrar los dos primeros niveles, según donde se hizo clic.) Estos casos (y otras variantes) ahora funcionan según lo esperado.</li></ul>|
|Ámbito|Borde|
|Versión|4.7.1|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Windows.Controls.Primitives.Popup.StaysOpen?displayProperty=nameWithType></li></ul>|

