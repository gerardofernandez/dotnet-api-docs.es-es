Usando una indización de basados en caracteres con la <xref:System.Text.StringBuilder.Chars%2A> propiedad puede ser muy lenta en las siguientes condiciones:

- El <xref:System.Text.StringBuilder> instancia es grande (por ejemplo, consta de varias decenas de miles de caracteres).
- El <xref:System.Text.StringBuilder> es "bloque". Es decir, las llamadas repetidas a métodos como <xref:System.Text.StringBuilder.Append%2A?displayProperty=nameWithType> automáticamente se han ampliado del objeto <xref:System.Text.StringBuilder.Capacity%2A?displayProperty=nameWithType> propiedad y fragmentos de nuevo asignadas de memoria a él.

Rendimiento se ve seriamente afectado ya que cada acceso carácter recorre toda la lista vinculada de fragmentos para buscar el búfer correcto para indizar en.

> [!NOTE]
>  Incluso para una gran "bloque" <xref:System.Text.StringBuilder> objeto utilizando el <xref:System.Text.StringBuilder.Chars%2A> propiedad para el acceso a uno o un número pequeño de caracteres basado en el índice tiene un efecto insignificante en el rendimiento; por lo general, resulta una **0(n)** operación. El impacto de rendimiento significativas se produce al recorrer en iteración los caracteres de la <xref:System.Text.StringBuilder> objeto, que es un **O(n^2)** operación. 

Si encuentra problemas de rendimiento al usar indexación basada en caracteres con <xref:System.Text.StringBuilder> objetos, puede utilizar cualquiera de las siguientes acciones:

- Convertir el <xref:System.Text.StringBuilder> instancia a un <xref:System.String> mediante una llamada a la <xref:System.Text.StringBuilder.ToString%2A> (método), tener acceso a los caracteres de la cadena.

- Copie el contenido de las existentes <xref:System.Text.StringBuilder> objeto a un nuevo un tamaño previo <xref:System.Text.StringBuilder> objeto. Mejora el rendimiento porque el nuevo <xref:System.Text.StringBuilder> objeto no está en bloque. Por ejemplo:

   ```csharp
   // sbOriginal is the existing StringBuilder object
   var sbNew = new StringBuilder(sbOriginal.ToString(), sbOriginal.Length);
   ```
   ```vb
   ' sbOriginal is the existing StringBuilder object
   Dim sbNew = New StringBuilder(sbOriginal.ToString(), sbOriginal.Length)
   ```
- Establecer la capacidad inicial de la <xref:System.Text.StringBuilder> objeto en un valor que es aproximadamente igual a su tamaño máximo esperado mediante una llamada a la <xref:System.Text.StringBuilder.%23ctor(System.Int32)> constructor. Tenga en cuenta que así asigna el bloque completo de aunque se utilicen memoria el <xref:System.Text.StringBuilder> rara vez alcanza su capacidad máxima.
