<!--
.. title: Cambios en las versiones de TWBlue
.. slug: changes-in-twblue-releases
.. date: 2021-10-28 09:26:48 UTC-05:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
-->

Nota: Había planeado publicar este artículo hoy, aunque los cambios descritos aquí se aplicaron de una manera completamente diferente debido a un problema que tuvimos con nuestras claves de la API de Twitter en el proyecto, por lo que todo el mundo se vio obligado a actualizar a la última versión de TWBlue. Sin embargo, Aún publico esto aquí para que tengas más información sobre por qué vamos a lanzar una única versión.

Hoy, después de muchos años de desarrollo y un par de años sin haber publicado aquí, nos complace anunciar un par de cambios que esperamos que afecten positivamente a la forma en que disfrutas de TWBlue, y lo que es más importante, a la frecuencia con la que podemos actualizar el software, añadir nuevas características y solucionar problemas de las versiones anteriores.

### Un poco de contexto

Antes del anuncio, es importante hablar un poco sobre algunos términos que hemos estado utilizando durante los últimos años aquí en TWBlue. Si no lo sabes, hace algunos años, empezamos a lanzar dos versiones diferentes de la misma aplicación. En ese momento, llamamos a esas versiones "estable" y "snapshot". La idea detrás de este razonamiento era que queríamos dar la posibilidad de elegir a nuestros usuarios, si querían utilizar una versión bien probada, totalmente traducida y documentada, que era la versión estable; o el código más actualizado que llegaba a nuestro repositorio, con las nuevas características, correcciones de errores y funciones todavía en fase de prueba que íbamos introduciendo antes de la siguiente estable. A esa versión la llamamos "Snapshot". Así, la gente que quería la versión estable se quedaba un poco desactualizada de todas las características que íbamos añadiendo, pero la versión era más madura y estaba más probada; mientras tanto, los usuarios de la Snapshot eran propensos a más bugs y a un menor rendimiento, pero normalmente tenían acceso a las características más nuevas. Al final, utilizábamos la versión snapshot para probar la siguiente estable, y nuestros usuarios participaban plenamente en ese proceso.

Sin embargo, después de 2019, tuvimos un momento difícil en el proyecto. En primer lugar, había muchos cambios que debíamos realizar si queríamos que TWBlue siguiera utilizando tecnología actualizada. Necesitábamos migrar a una de las versiones de Pytohn 3, ya que Python 2 fue descontinuado hace un tiempo; necesitábamos reemplazar el módulo que usamos para comunicarnos con Twitter -ya que Twython, el módulo que usábamos antes, parece estar abandonado, y mientras tanto dejamos de soportar Windows XP y reemplazamos nuestro motor de reproducción de audio completamente. Al mismo tiempo, recibimos menos contribuciones de la comunidad en nuestro repositorio, ya que todas las personas que contribuyen al proyecto lo hacen durante su tiempo libre y normalmente tienen días bastante ocupados.

El hecho de tener más trabajo, menos gente trabajando en el proyecto y situaciones de la vida que hacen que en general no podamos estar trabajando en el proyecto como nos gustaría, tuvo algunas consecuencias. La primera y más importante fue que no pudimos publicar ni snapshot ni versiones estables en mucho tiempo debido a la magnitud de los cambios que estábamos realizando, por lo que mucha gente pensó que el proyecto estaba abandonado, a pesar de estar generalmente activo en los repositorios de código fuente. Una vez que tuvimos algo que podíamos publicar como una nueva versión Snapshot, las diferencias contra la última versión estable, la 0.95, eran demasiado significativas, por lo que sabíamos desde la primera snapshot  construida con Python 3 que publicamos, que seríamos incapaces de liberar una nueva versión estable como una actualización de la versión existente porque todo se rompería. En resumen, tanto la versión de Python 2 (0.95 o la estable lanzada en 2019) como todas las nuevas snapshot (versiones de Python 3) no se pueden mezclar, por lo que la actualización automática de la versión estable no sería posible. Además, las nuevas versiones de snapshot introdujeron muchas cosas que hicieron que no pudiéramos actualizar la estable, como una nueva base de datos para almacenar los tweets, que rompería la estable, cambios en la configuración de los proxies que tampoco son compatibles con los valores de configuración de las estables, y algunos otros cambios que podrían romper otras características ofrecidas por el proyecto debido a la diferencia entre las versiones de Python.

Otra consecuencia de nuestro (considerablemente extraño) calendario de lanzamientos fue que muy a menudo, la gente tiende a pensar en las versiones snapshot como código inestable o peligroso. Hace un par de semanas, empecé a recomendar a la gente que usara la última versión snapshot en lugar de la estable actual, porque estábamos básicamente 2 años por delante en desarrollo, características y correcciones que en 2019, pero recibí muchas preguntas sobre la estabilidad de las snapshots actuales. Por eso pensé que debíamos hacer algo con este problema.
Dado que hoy en día las versiones snapshot son mucho más estables que el instalador, el portable u otros paquetes que distribuimos en 2019 como "versión estable actual". Pensé que ya no debíamos llamar a las versiones de TWBlue como "snapshots", ya que estas son mucho más estables, tienen mejor rendimiento y generalmente no tienen errores presentes aún en las versiones que considerábamos como versión estable en 2019.

### ¿Qué cambiará?

Últimamente he estado bastante ocupado con muchas otras cosas tanto en mi vida personal como en mi trabajo. Entre ellas, estoy creando una empresa de software unipersonal para poder acceder a más oportunidades en México, el país donde vivo. Probablemente, si usas TWBlue, notarás un cambio de nombre en la sección sobre la aplicación. Aunque será un cambio menor, porque todo lo demás será igual. En cuanto a las versiones de TWBlue, vamos a hacerlo mucho más fácil para todos publicando una sola versión, que se actualizará regularmente para añadir nuevas características, correcciones de errores y traducciones. Ya no mantendremos versiones separadas en función de la estabilidad del código, porque consideramos que con la base de código actual, TWBlue es lo suficientemente estable como para mantener una versión unificada y actualizar esta versión con las últimas características que proporciona Twitter.

También vamos a cambiar nuestro sistema de versiones a la publicación de versiones por calendario. Esto significa que en lugar de lanzar el software basado en la versión mayor y menor, como lo hacíamos antes, empezaremos a lanzar las versiones de TWBlue basadas en la fecha de finalización del lanzamiento. Así, muy pronto verás la versión 2021.10.26 de TWBlue, por ejemplo, lo que debería hacer más fácil para la gente identificar cuándo se generó exactamente la versión.

### Conclusión

Con estos cambios, esperamos tener más tiempo para escribir, probar y entregar características en el software en lugar de preocuparnos por cuándo debemos congelar una versión específica y cuándo debemos lanzar más snapshots. Además, esperamos que esto haga que el proyecto sea más activo entre la comunidad y deje de dar la impresión de abandono por parte de la gente que lo utiliza.

Por último, pero no por ello menos importante, quería tomarme el tiempo para darles las gracias a todos, usuarios, colaboradores, traductores y diseñadores de paquetes de sonidos por poner lo que está en sus posibilidades para hacer de este proyecto la gran aplicación en la que se está convirtiendo. Cuando empecé a programar esto, sólo en español y como un proyecto para divertirme y aprender un poco más sobre programación en Python, nunca imaginé que este proyecto duraría 8 años. Y mientras Twitter siga existiendo y permitiendo a los desarrolladores de terceros escribir apps para su plataforma, espero que podamos ver muchos años más de este proyecto, que, entre otras cosas, está traducido a más de 19 idiomas por un grupo de gente experimentada, haciendo que muchos más usuarios puedan disfrutar de una buena experiencia en Twitter. Como desarrollador principal del proyecto, todos ustedes me animan a implementar todos los cambios para que el software sea mejor. Gracias a todos y esperemos que sean muchos años más.