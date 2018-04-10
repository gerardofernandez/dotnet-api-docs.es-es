### <a name="wpf-spell-checking-in-text-enabled-controls-will-not-work-in-windows-10-for-languages-not-in-the-oss-input-language-list"></a>Ortográfica de WPF en controles de texto no funcionará en Windows 10 idiomas no en la lista de idiomas de entrada de los sistemas operativos

|   |   |
|---|---|
|Detalles|Cuando se ejecuta en Windows 10, el corrector ortográfico no funcione para los controles WPF habilitados para texto porque ortográfica de plataforma solo está disponible para idiomas que aparecen en la lista de idiomas de entrada. En Windows 10, al agregar un idioma a la lista de teclados disponibles, Windows descarga e instala automáticamente una función correspondiente en el paquete (Demand, FOD) que proporciona capacidades de revisión ortográfica. Al agregar el idioma a la lista de idiomas de entrada, se admitirá el corrector ortográfico.|
|Sugerencia|Tenga en cuenta que el idioma o el texto que se les comprobará el corrector debe agregarse como un idioma de entrada para el corrector ortográfico para que funcione en Windows 10.|
|Ámbito|Borde|
|Versión|4.6|
|Tipo|Tiempo de ejecución|

