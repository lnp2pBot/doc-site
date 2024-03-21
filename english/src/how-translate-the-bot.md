# How to translate the bot?

To translate [lnp2pBot](https://t.me/lnp2pBot), you must do a pull request [(Pull Request or PR)](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) on the GitHub repository [https://github.com/lnp2pBot/bot](https://github.com/lnp2pBot/bot) by adding a new `.yaml` file in [https://github.com/lnp2pBot/bot/tree/main/locales](https://github.com/lnp2pBot/bot/tree/main/locales) with the translation of the bot strings.

The new `yaml` file should be named using language codes [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639_language_codes), for example, in Spanish it is `es`, then the name should be `es.yaml`.

You can use as a guide [https://github.com/lnp2pBot/bot/blob/main/locales/en.yaml](https://github.com/lnp2pBot/bot/blob/main/locales/en.yaml), copy it and modify only the texts that are not a key (the keys are the ones before the colon : ).

You can also use as a reference some previously added language PR: [https://github.com/lnp2pBot/bot/pull/460](https://github.com/lnp2pBot/bot/pull/460).

If you are not a technical person, don't worry, just download `en.yaml` or the translation where you feel most comfortable, translate it and send it to some administrator of the [telegram group](https://t.me/lnp2pbotHelp).
