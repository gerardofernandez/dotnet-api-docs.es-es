### <a name="calling-createdefaultauthorizationcontext-with-a-null-argument-has-changed"></a>Llamando a CreateDefaultAuthorizationContext con un argumento nulo ha cambiado

|   |   |
|---|---|
|Detalles|La implementación de la <xref:System.IdentityModel.Policy.AuthorizationContext?displayProperty=name> devuelto por una llamada a la <xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=name> con un authorizationPolicies null argumento ha cambiado su implementación en .NET Framework 4.6.|
|Sugerencia|En raras ocasiones, las aplicaciones WCF que usan la autenticación personalizada pueden sufrir diferencias de comportamiento. En estos casos, es posible restaurar el comportamiento anterior de dos maneras:<ol><li>Vuelva a compilar la aplicación para que se dirija a una versión anterior a .NET Framework 4.6. Para los servicios hospedados en IIS, use la &lt;httpRuntime targetFramework =&quot;x.x&quot;  / &gt; elemento como destino una versión anterior de .NET Framework.</li><li>Agregue la siguiente línea a la sección <code>&lt;appSettings&gt;</code> del archivo app.config: <code>&lt;add key=&quot;appContext.SetSwitch:Switch.System.IdentityModel.EnableCachedEmptyDefaultAuthorizationContext&quot; value=&quot;true&quot; /&gt;</code>.</li></ol>|
|Ámbito|Secundaria|
|Versión|4.6|
|Tipo|Redestinación|
|API afectadas|<ul><li><xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=nameWithType></li></ul>|

