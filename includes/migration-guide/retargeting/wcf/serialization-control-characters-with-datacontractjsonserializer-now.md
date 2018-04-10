### <a name="serialization-of-control-characters-with-datacontractjsonserializer-is-now-compatible-with-ecmascript-v6-and-v8"></a>Serialización de los caracteres de control con DataContractJsonSerializer ahora es compatible con ECMAScript V6 y V8

|   |   |
|---|---|
|Detalles|En .NET framework 4.6.2 y versiones anteriores, el <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=name> no serializar algunos caracteres de control especiales, como \b y \f, \t, de manera que es compatible con los estándares de ECMAScript V6 y V8. A partir de la 4.7 de .NET Framework, la serialización de estos caracteres de control es compatible con ECMAScript V6 y V8.|
|Sugerencia|Para las aplicaciones que tienen como destino la 4.7 de .NET Framework, esta característica está habilitada de forma predeterminada. Si no desea este compartimiento, puede rechazar esta característica agregando la siguiente línea a la sección <code>&lt;runtime&gt;</code> del archivo app.config o web.config:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Runtime.Serialization.DoNotUseECMAScriptV6EscapeControlCharacter=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Ámbito|Borde|
|Versión|4.7|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlDictionaryWriter,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlWriter,System.Object)?displayProperty=nameWithType></li></ul>|

