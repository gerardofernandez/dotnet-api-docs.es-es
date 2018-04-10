### <a name="wpf-pointer-based-touch-stack"></a>Pila de basada en puntero táctil WPF

|   |   |
|---|---|
|Detalles|Este cambio se agrega la posibilidad de habilitar una WM_POINTER opcional basadas pila táctil o lápiz WPF.  Los desarrolladores que no habilitan explícitamente esto no deberían ver ningún cambio en el comportamiento de táctil o lápiz WPF. Actual problemas conocidos con WM_POINTER opcional basada en pila táctil/lápiz:<ul><li>No se admiten las entradas manuscritas en tiempo real.</li><li>Entrada manuscrita y StylusPlugins seguirá funcionando, se procesarán en el subproceso de interfaz de usuario que puede dar lugar a un rendimiento deficiente.</li><li>Cambios de comportamiento debido a cambios en la promoción de los eventos de toque/lápiz a eventos del mouse</li><li>Manipulación puede comportarse de forma diferente</li><li>Arrastrar y colocar no se mostrará la información apropiada para la entrada táctil</li><li>Esto no afecta a la entrada de lápiz</li><li>Arrastrar y colocar ya no se puede iniciar en eventos de entrada táctil/lápiz</li><li>Esto puede hacer que la aplicación de detenga hasta que se detecte la entrada del mouse.</li><li>En su lugar, los desarrolladores deben iniciar Arrastrar y colocar en los eventos del mouse.</li></ul>|
|Sugerencia|Los desarrolladores que deseen habilitar esta pila pueden agregar/merge lo siguiente al archivo de App.config de su aplicación:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Input.Stylus.EnablePointerSupport=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>Si elimina este o establecer el valor en false se desactivará esta pila opcional. Tenga en cuenta que esta pila está disponible solo en los creadores de actualización de Windows 10 y versiones posteriores.|
|Ámbito|Borde|
|Versión|4.7|
|Tipo|Redestinación|

