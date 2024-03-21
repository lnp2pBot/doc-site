# How to translate and collaborate with documentation?

The [lnp2pBot](https://t.me/lnp2pBot) documentation has been created with [mdBook](https://rust-lang.github.io/mdBook), a versatile tool that enables us to organize it clearly and coherently, this includes the creation of chapters, sections, cross-links, etc, ensuring fluid navigation and easy comprehension of the content.

Below, we provide a step-by-step guide on how to translate the documentation. This guide can also be useful if you wish to add more content or improve existing material:

1) **Install Rust:** [https://www.rust-lang.org/tools/install](https://www.rust-lang.org/tools/install)

2) **Install mdBook:**

```bash
$ cargo install mdbook
```

3) **Clone the repository and create a new language directory:** Clone the repository [https://github.com/lnp2pBot/doc-site](https://github.com/lnp2pBot/doc-site) and then create a new directory for the language you want to translate the documentation into, based on the existing English or Spanish directory (these are the most frequently updated).

```bash
$ git clone https://github.com/lnp2pBot/doc-site.git

$ cd doc-site

$ cp -r english <your-language>
```

4) **Modify the `book.toml` file:**
You must set the `language` and `title` parameters in the `book.toml` file. For `language`, you must use the language codes [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639_language_codes); and fot `title`, replace "Learn" with its equivalent in your language.

language = "en"
title = "Learn @lnp2pBot"


5) **View the Book Locally:** Once inside the directory that we have copied, you can see what the book looks like locally using the following command:

```bash
$ cd <your-language>

$ mdbook serve
```

Then, open [http://localhost:3000](http://localhost:3000) in your web browser to view the created workbook.

6) **Start Translation:** To begin translating the documentation, access each `.md` file within the `src` directory. Any changes you make will automatically appear updated in the book at [http://localhost:3000](http://localhost:3000) while mdBook is running.

- In the `SUMMARY.md` file, you will find the structure of the book's chapters. You only need to translate the chapter titles, enclosed in brackets [ ], without modifying the links, enclosed in parentheses ( ).

- To replace an image or gif with one in your language place it in `/assets/images/` and delete the original file, but give the new one the same name.

- Do not translate `.md` file names or links.

7) **Send a Pull Request (PR):** Once you have finished the translation submit a pull request [(Pull Request or PR)](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) in the GitHub repository [https://github.com/lnp2pBot/doc-site](https://github.com/lnp2pBot/doc-site).

### Tips
- Check out this guide on [How to format texts with markdown](https://rust-lang.github.io/mdBook/format/markdown.html).
- You could do the translations without using mdBook by simply translating each file and submit the PR, although that way you could make mistakes
- If you encounter difficulties following this tutorial, please contact an administrator of the [telegram group](https://t.me/lnp2pbotHelp) for assistance.
