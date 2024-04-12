# Desarrollo

_Esta guía se basa en la [guía de contribución de Bisq](https://github.com/bisq-network/bisq/blob/master/CONTRIBUTING.md)._

Cualquiera es bienvenido a contribuir con [lnp2pBot](https://t.me/lnp2pBot). Si estás buscando por dónde empezar, echa un vistazo a la [lista de buenos primeros problemas](https://github.com/grunch/p2plnbot/issues?q=is%3Aopen+is%3Aissue+label%3A"good+first+issue").

### Canales de Comunicación
La mayoría de la comunicación sobre [lnp2pBot](https://t.me/lnp2pBot) ocurre en el [grupo de Telegram](https://t.me/lnp2pbotHelp). La discusión sobre cambios de código ocurre en los [problemas](https://github.com/lnp2pBot/bot/issues) y [solicitudes de extracción](https://github.com/lnp2pBot/bot/pulls) de GitHub.

### Flujo de Trabajo del Contribuidor
Todos los contribuidores de [lnp2pBot](https://t.me/lnp2pBot) envían cambios a través de solicitudes de extracción. El flujo de trabajo es el siguiente:

- Hacer un _fork_ del repositorio.
- Crear una rama temática a partir de la rama `main`.
- Hacer _commits_ de los parches.
- Unificar _commits_ redundantes o innecesarios.
- Enviar una solicitud de extracción desde la rama de tu tema a la rama `main` del repositorio principal
- Realizar cambios en la solicitud de extracción si los revisores lo solicitan y solicitar una revisión.

Las solicitudes de extracción deben centrarse en un único cambio. No mezcles, por ejemplo, refactorizaciones con una corrección de errores o la implementación de una nueva característica. Esta práctica facilita que los demás contribuidores revisen cada solicitud de extracción.

### Revisión de Solicitudes de Extracción
[lnp2pBot](https://t.me/lnp2pBot) sigue el flujo de trabajo de revisión establecido por el proyecto Bitcoin Core. Lo siguiente está adaptado de la [documentación para contribuidores de Bitcoin Core](https://github.com/bitcoin/bitcoin/blob/master/CONTRIBUTING.md#peer-review):

Cualquiera puede participar en la revisión de pares, que se expresa mediante comentarios en la solicitud de extracción. Generalmente, los revisores revisarán el código en busca de errores obvios, además de probar el conjunto de parches y opinar sobre los méritos técnicos del parche. Los mantenedores del proyecto tienen en cuenta la revisión de pares al determinar si hay consenso para fusionar una solicitud de extracción (recuerda que las discusiones pueden haberse dispersado en GitHub y Telegram). El siguiente lenguaje se usa dentro de los comentarios de la solicitud de extracción:

`ACK` significa "He probado el código y estoy de acuerdo en que debería fusionarse"  
`NACK`  significa "Discrepo en que esto deba fusionarse" y debe ir acompañado de una justificación técnica sólida. Los NACKs sin justificación acompañante pueden ser ignorados  
`utACK`  significa "No he probado el código, pero lo he revisado y parece estar bien, estoy de acuerdo en que puede fusionarse"  
 `Concept ACK`significa "Estoy de acuerdo en el principio general de esta solicitud de extracción"  
`Nit`  se refiere a problemas triviales, a menudo no bloqueantes.  

Ten en cuenta que las solicitudes de extracción marcadas como `NACK` y/o `Change requested` en GitHub se cierran después de 30 días si no se abordan.

### Convenciones de estilo y codificación
#### Estándares de codificación
Seguimos la [guía de estilo de JavaScript de Airbnb](https://github.com/airbnb/javascript) para tener un código más limpio.

#### Configurar el nombre de usuario y correo electrónico de Git
Consulta [https://help.github.com/articles/setting-your-username-in-git/](https://help.github.com/articles/setting-your-username-in-git/) para obtener instrucciones.

#### Escribir mensajes de confirmación bien formados
Desde [https://chris.beams.io/posts/git-commit/#seven-rules](https://chris.beams.io/posts/git-commit/#seven-rules):

- Separar el asunto del cuerpo con una línea en blanco
- Limitar la línea de asunto a 50 caracteres (*)
- Poner en mayúscula la línea de asunto
- No terminar la línea de asunto con un punto
- Usar el modo imperativo en la línea de asunto
- Envolver el cuerpo en 72 caracteres (*)
- Usar el cuerpo para explicar el qué y el porqué frente al cómo

#### Firmar tus commits con GPG
Consulta [https://github.com/blog/2144-gpg-signature-verification](https://github.com/blog/2144-gpg-signature-verification) para obtener antecedentes y [https://help.github.com/articles/signing-commits-with-gpg/](https://help.github.com/articles/signing-commits-with-gpg/) para obtener instrucciones.


#### Mantener limpio el historial de Git
Es muy importante mantener el historial de git claro, ligero y fácilmente navegable. Esto significa que los contribuyentes deben asegurarse de que sus solicitudes de extracción incluyan solo confirmaciones significativas (si son redundantes o se agregaron después de una revisión, deben eliminarse) y no incluir _ninguna confirmación de fusión_.
