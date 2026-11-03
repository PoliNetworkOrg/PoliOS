# Contribuire / Contributing

## 🇮🇹 Italiano

Grazie per l'aiuto! PoliOS è un progetto di studenti e ha bisogno di tester.

**Segnalare un problema** — apri una [segnalazione](../../issues/new/choose) con il modulo "Segnala un problema": dove l'hai provato, cosa ti aspettavi, cosa è successo. Screenshot e messaggi di errore aiutano molto.

**Aggiungere o correggere un corso** — modifica [`polios-cubic/welcome/courses.conf`](polios-cubic/welcome/courses.conf) con una pull request:
- una sezione `[id-corso]` per gruppo di corsi (solo lettere minuscole, numeri e `-`);
- `title`/`description` in italiano e, se puoi, `title_en`/`description_en` in inglese;
- `apt` (pacchetti Ubuntu 24.04), `flatpak` (ID Flathub), oppure `extra` (ricette incluse: per ora solo `google-chrome`);
- niente software proprietario che non si possa ridistribuire, niente URL o comandi: l'elenco può solo *nominare* pacchetti;
- prima di aprire la PR controlla: `python3 polios-cubic/welcome/polios-welcome-helper --check polios-cubic/welcome/courses.conf` (su Ubuntu/Mint 24.04 verifica anche che i pacchetti apt esistano). Lo stesso controllo gira in automatico sulla PR.

Ricorda: ciò che entra in `main` arriva **subito** sui computer degli studenti, per questo ogni modifica richiede una revisione.

**Modificare il kit di compilazione** — vedi [`polios-cubic/README.md`](polios-cubic/README.md). Test: `python3 -m unittest discover polios-cubic/welcome/tests`.

## 🇬🇧 English

Thanks for helping! PoliOS is a student project and needs testers.

**Report a problem** — open an [issue](../../issues/new/choose) with the "Report a problem" form: where you ran it, what you expected, what happened. Screenshots and error messages help a lot.

**Add or fix a course** — edit [`polios-cubic/welcome/courses.conf`](polios-cubic/welcome/courses.conf) in a pull request:
- one `[course-id]` section per group of courses (lowercase letters, digits and `-` only);
- `title`/`description` in Italian and, if you can, `title_en`/`description_en` in English;
- `apt` (Ubuntu 24.04 packages), `flatpak` (Flathub IDs), or `extra` (built-in recipes: only `google-chrome` for now);
- no proprietary software that can't be redistributed, no URLs or commands: the list can only *name* packages;
- before opening the PR run: `python3 polios-cubic/welcome/polios-welcome-helper --check polios-cubic/welcome/courses.conf` (on Ubuntu/Mint 24.04 it also checks that the apt packages exist). The same check runs automatically on the PR.

Remember: what lands in `main` reaches students' computers **right away**, so every change needs a review.

**Changing the build kit** — see [`polios-cubic/README.md`](polios-cubic/README.md). Tests: `python3 -m unittest discover polios-cubic/welcome/tests`.
