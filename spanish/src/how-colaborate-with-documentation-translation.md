# ¿Cómo traducir y colaborar con la documentación?

La documentación de [lnp2pBot](https://t.me/lnp2pBot) se ha creado con [mdBook](https://rust-lang.github.io/mdBook), una herramienta versátil que nos permite organizarla de manera clara y coherente, esto incluye la creación de capítulos, secciones, enlaces cruzados etc, logrando una navegación fluida y una comprensión fácil del contenido.

A continuación explicamos paso a paso cómo traducir la documentación, aunque también te puede ser útil si deseas agregar más contenido o mejorar el material existente:

1) **Instala Rust:** [https://www.rust-lang.org/tools/install](https://www.rust-lang.org/tools/install)

2) **Instala mdBook:**

```bash
$ cargo install mdbook
```

3) **Clona el repositorio y crea un nuevo directorio del idioma:** Clona el repositorio [https://github.com/lnp2pBot/doc-site](https://github.com/lnp2pBot/doc-site) y luego crea un nuevo directorio para el idioma al que deseas traducir la documentación basado en el directorio existenete en inglés o español (son los que se actualizan con mayor frecuencia).

```bash
$ git clone https://github.com/lnp2pBot/doc-site.git

$ cd doc-site

$ cp -r english <tu-idioma>
```

4) **Modifica el archivo `book.toml`:**
Debes establecer los parámetros `language` y `title` en el archivo `book.toml`. Para `language` debes usar los códigos de idioma [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639_language_codes); y en `title` debes sustituir "Learn" por su equivalente en tu idioma.  

language = "en"  
title = "Learn @lnp2pBot"


5) **Visualiza el Libro Localmente:** Una vez dentro del directorio que hemos copiado, puedes ver cómo se ve el libro localmente utilizando el siguiente comando:

```bash
$ cd <tu-idioma> 

$ mdbook serve
```

Luego, abre [http://localhost:3000](http://localhost:3000) en tu navegador web para visualizar el libro creado.

6) **Comienza la Traducción:** Para comenzar a traducir la documentación accede a cada archivo `.md` dentro del directorio `src`. Los cambios que realices se mostrarán automáticamente actualizados en el libro en [http://localhost:3000](http://localhost:3000) mientras mdBook esté en ejecución. 

- En el archivo `SUMMARY.md`, encontrarás la estructura de los capítulos del libro. Solo necesitas traducir los títulos de los capítulos, encerrados entre corchetes [ ], sin modificar los enlaces, encerrados entre paréntesis ( ).

- Para remplazar alguna imagen o gif por uno en tu idioma debes ponerlo en `/assets/images/` y eliminar el archivo original, pero ponerle su mismo nombre al nuevo.

- No traduzcas los nombres de los archivos `.md` ni los enlaces.

7) **Envía una Solicitud de Extracción (Pull Request o PR):** Cuando hayas terminado la traducción debes hacer una solicitud de extracción [(Pull Request o PR)](https://docs.github.com/es/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) en el repositorio de GitHub [https://github.com/lnp2pBot/doc-site](https://github.com/lnp2pBot/doc-site).

### Tips
- Consulta esta guía sobre [Cómo dar formato a los textos con markdown](https://rust-lang.github.io/mdBook/format/markdown.html).
- Podrías hacer las traducciones sin usar mdBook simplemente traduciendo cada archivo y subiendo el PR, aunque de esa forma podrías cometer errores
- Si encuentras dificultades al seguir este tutorial, contacta con algún administrador del [grupo de telegram](https://t.me/lnp2pbotHelp) para recibir ayuda.
