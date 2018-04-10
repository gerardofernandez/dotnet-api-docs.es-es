### <a name="aspnet-mvc-now-escapes-spaces-in-strings-passed-in-via-route-parameters"></a>Ahora, ASP.NET MVC escapes espacios de cadenas que se pasa a través de parámetros de ruta

|   |   |
|---|---|
|Detalles|Para cumplir con RFC 2396, ahora se aplican caracteres de escape a los espacios de las rutas de acceso al rellenar parámetros de acción desde una ruta. Por tanto, mientras que <code>/controller/action/some data</code> antes coincidía con la ruta <code>/controller/action/{data}</code> y proporcionaba <code>some data</code> como parámetro de datos, ahora proporciona <code>some%20data</code>.|
|Sugerencia|Debería actualizarse el código para no eliminar las secuencias de escape de los parámetros de las cadenas desde una ruta. Si se necesita el identificador URI original, puede tener acceso mediante el <xref:System.Net.HttpWebRequest.RequestUri>. OriginalString API.|
|Ámbito|Secundaria|
|Versión|4.5.2|
|Tipo|Tiempo de ejecución|
|API afectadas|<ul><li><xref:System.Web.Mvc.RouteAttribute.%23ctor(System.String)?displayProperty=nameWithType></li></ul>|

